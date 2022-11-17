# start.gg Bracket Chroma Key for OBS
Here's a simple browser source CSS snippet for chroma-keying start.gg brackets. It takes the start.gg bracket and turns it into a more compact, chroma-keyable version. This makes it usable for any event and bracket type without needing to be rewritten for each size or type of bracket.

# Snippets
The snippets come first, then scroll down further for proper instructions on using them.
## Black backgrounds behind rounds
### Image Example
![image](https://user-images.githubusercontent.com/22358804/202442612-8684abba-1efc-4e65-8c92-772fdce815e6.png)
### CSS
```css
body { background-color: rgba(0, 0, 0, 0); margin: 0px auto; zoom:400% }

.bracket {
  position: fixed;
  padding: 15px;
  overflow: auto;
  z-index: 100000;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgb(255, 0, 255 );
}

.root-sggBAddL .timeContainer-sggSCTWl {
  color: rgb(170,170,170);
  line-height: var(--line-height--lg);
  display:none;
}

.root-sggBAddL {
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: rgb(20,20,20);
  color: white;
  line-height: 30px;
  text-align: center;
}

.root-sggBAddL .titleContainer-sggCtPJ- .title-sggP5PgL {
  font-size: var(--font-size--md);
  font-weight: var(--font-weight--bold);
  width: 100%;
}

.root-sggBAddL .timeContainer-sggSCTWl {
  color: rgba(170,170,170);
  line-height: var(--line-height--lg);
}

.RoundHeader-sggW-5vC {
  padding-bottom: 0;
  margin-bottom: 8px;
  border-bottom: 0px;
  display: inline-block;
}

.match-affix-wrapper .match-label {
  position: absolute;
  top: 0;
  bottom: 0;
  height: 16px;
  margin: auto;
  color: #fff;
  background: black;
  left: -14px;
  font-size: 10px;
}
```
## Clear backgrounds behind rounds
### Image Example
![image](https://user-images.githubusercontent.com/22358804/202442883-a4a8cb5d-aa3e-4c4f-bff8-30f0afa02d24.png)
### CSS
```css
body { background-color: rgba(0, 0, 0, 0); margin: 0px auto; zoom:400% }

.bracket {
  position: fixed;
  padding: 15px;
  overflow: auto;
  z-index: 100000;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgb(255, 0, 255 );
}

.root-sggBAddL .timeContainer-sggSCTWl {
  color: rgb(170,170,170);
  line-height: var(--line-height--lg);
  display:none;
}

.root-sggBAddL {
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: rgb(255,0,255);
  color: white;
  line-height: 30px;
  text-align: center;
}

.root-sggBAddL .titleContainer-sggCtPJ- .title-sggP5PgL {
  font-size: var(--font-size--md);
  font-weight: var(--font-weight--bold);
  width: 100%;
}

.root-sggBAddL .timeContainer-sggSCTWl {
  color: rgba(170,170,170);
  line-height: var(--line-height--lg);
}

.RoundHeader-sggW-5vC {
  padding-bottom: 0;
  margin-bottom: 8px;
  border-bottom: 0px;
  display: inline-block;
}

.match-affix-wrapper .match-label {
  position: absolute;
  top: 0;
  bottom: 0;
  height: 16px;
  margin: auto;
  color: #fff;
  background: black;
  left: -14px;
  font-size: 10px;
}
```
# Usage

- Input a start.gg bracket link into an OBS browser source 
- Set the source size to 4096x2300 (larger sizes improve the chroma key)
- Copy in a custom CSS snippet from this repository
- Use the “Interact” button on OBS to click away the cookies banner if needed
- Add a chroma key filter. \
  **Recommended settings**:
  - Color: Magenta
  - Similarity: 365
  - Smoothness: 1
  - Key Color Spill Reduction: 400
- If the bracket is too big, scrollbars will appear. Use alt+click dragging on the source handles to crop them out
  - Use the "Interact" button to use the scrollbars to move bracket around as needed
- Manually resize and center the source in the preview
- Right click the source and set "Scale Filtering" to "Area"
