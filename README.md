## Welcome to Cabsoftware GitHub Pages
Cabsoftware make paperless solution at South Korea.

RxEnterprise is the name of paperless solution and based on java and c.
Cabsoftware focus on finance and insulance market paperless workflow since 2012.

### Paperless Solution

There are 3 devision :
 - rxDirect
 - rxEform
 - rxSign

```
/**
 * [num2han 숫자를 한글로 변환]
 * @param  {[integer]} num [숫자]
 * @return {[string]}      [한글 숫자]
 *
 * @origin http://www.phpschool.com/gnuboard4/bbs/board.php?bo_table=tipntech&wr_id=14981
 */
function num2han(num){
    var i, j=0, k=0;
    var han1 = ["","일","이","삼","사","오","육","칠","팔","구"];
    var han2 = ["","만","억","조","경","해","시","양","구","간"];
    var han3 = ["","십","백","천"];
    var result = "", hangul = num + "";
    var pm = ""; // 부호
    var str = [], str2="";
    var strTmp = [];

    if(Number(num)===0){
        return "영";
    }

    if(hangul.substring(0,1)==="-"){
        pm = "마이너스 ";
        hangul = hangul.substring(1, hangul.length);
    }

    if(hangul.length > han2.length*4){
        return "too much number";
    }

    for(i=hangul.length; i > 0; i=i-4){
        str[j] = hangul.substring(i-4,i);

        for(k=str[j].length;k>0;k--){
            strTmp[k] = (str[j].substring(k-1,k))?str[j].substring(k-1,k):"";
            strTmp[k] = han1[parseInt(strTmp[k])];

            if(strTmp[k]){
                strTmp[k] += han3[str[j].length-k];
            }

            str2 = strTmp[k] + str2;
        }

        str[j] = str2;

        if(str[j]){
            result = str[j]+han2[j]+result;
        }

        // 4자리마다 한칸씩 띄고 보여준다.
        //result = (str[j])? " "+str[j]+han2[j]+result : " " + result;
        j++;
        str2 = "";
    }

    return pm + result;
}
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### RoadMap

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/cabsoft/docs/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact
1.[마크다운 링크](test)

Having trouble with RxEnterprise Solution? Check out our [documentation](http://www.cabsoftware.com/reportexpress/docs/api/) and we’ll help you sort it out.
