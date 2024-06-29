<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>論理的満足</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            color: #333;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        h1 {
            text-align: center;
            margin-top: 20px;
            color: #555;
        }
        .question-container {
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            margin: 20px auto;
            max-width: 600px;
        }
        p {
            margin: 0 0 10px;
            line-height: 1.6;
        }
        form {
            margin-top: 20px;
        }
        input[type="radio"] {
            display: none;
        }
        label {
            display: block;
            cursor: pointer;
            margin-bottom: 10px;
            padding: 10px;
            border-radius: 5px;
            background-color: #f5f5f5;
            transition: background-color 0.3s ease;
        }
        label:hover {
            background-color: #e0e0e0;
        }
        input[type="button"] {
            background-color: #4caf50;
            color: #fff;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        input[type="button"]:hover {
            background-color: #45a049;
        }
        .result {
            font-weight: bold;
            margin-top: 10px;
        }
        .explanation {
            display: none;
            margin-top: 10px;
        }
        .correct {
            color: #4caf50;
        }
        .incorrect {
            color: #f44336;
        }
        /* 追加のスタイル */
        input[type="radio"]:checked + label {
            background-color: #4caf50;
            color: #fff;
        }
    </style>
</head>
<body>
    <h1>論理的満足</h1>

    <!-- 問題1 -->
    <div class="question-container" id="question1">
        <p>論理的満足とは何を意味するでしょうか？</p>
        <form>
            <input type="radio" id="q1_option1" name="q1" value="1">
            <label for="q1_option1">商品が安い価格で購入できた時</label><br>
            <input type="radio" id="q1_option2" name="q1" value="2">
            <label for="q1_option2">商品の機能が充実している時</label><br>
            <input type="radio" id="q1_option3" name="q1" value="3">
            <label for="q1_option3">信頼できるブランドからの購入時</label><br>
            <input type="radio" id="q1_option4" name="q1" value="4">
            <label for="q1_option4">商品のデザインが優れている時</label>
        </form>
        <p class="result" id="result1"></p>
        <p class="explanation" id="explanation1">
            解説: 論理的満足は、商品の機能が充実している時や、安価で購入できた時に感じる満足を指します。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q1', 2, 'result1', 'explanation1')">
    </div>

    <!-- 問題2 -->
    <div class="question-container" id="question2">
        <p>感情的満足は何を意味するでしょうか？</p>
        <form>
            <input type="radio" id="q2_option1" name="q2" value="1">
            <label for="q2_option1">安価で購入できた時</label><br>
            <input type="radio" id="q2_option2" name="q2" value="2">
            <label for="q2_option2">商品の機能が充実している時</label><br>
            <input type="radio" id="q2_option3" name="q2" value="3">
            <label for="q2_option3">信頼できるブランドからの購入時</label><br>
            <input type="radio" id="q2_option4" name="q2" value="4">
            <label for="q2_option4">愛着を感じる状況の時</label>
        </form>
        <p class="result" id="result2"></p>
        <p class="explanation" id="explanation2">
            解説: 感情的満足は、商品やブランドに対する信頼や愛着を感じる状況での満足を指します。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q2', 4, 'result2', 'explanation2')">
    </div>

    <!-- 問題3 -->
    <div class="question-container" id="question3">
        <p>顧客がサービスに満足するために重要な要素として、次のうちどれが正しいでしょうか？</p>
        <form>
            <input type="radio" id="q3_option1" name="q3" value="1">
            <label for="q3_option1">安価なサービス料金</label><br>
            <input type="radio" id="q3_option2" name="q3" value="2">
            <label for="q3_option2">高品質なサービスの提供</label><br>
            <input type="radio" id="q3_option3" name="q3" value="3">
            <label for="q3_option3">多様なサービスオプション</label><br>
            <input type="radio" id="q3_option4" name="q3" value="4">
            <label for="q3_option4">サービスの速度と効率</label>
        </form>
        <p class="result" id="result3"></p>
        <p class="explanation" id="explanation3">
            解説: 顧客満足に重要な要素として、高品質なサービスの提供が挙げられます。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q3', 2, 'result3', 'explanation3')">
    </div>

    <!-- 問題4 -->
    <div class="question-container" id="question4">
        <p>サービス品質を向上させるために使用されるモデルは何でしょうか？</p>
        <form>
            <input type="radio" id="q4_option1" name="q4" value="1">
            <label for="q4_option1">狩野モデル</label><br>
            <input type="radio" id="q4_option2" name="q4" value="2">
            <label for="q4_option2">マーケティングミックス</label><br>
            <input type="radio" id="q4_option3" name="q4" value="3">
            <label for="q4_option3">BCGマトリックス</label><br>
            <input type="radio" id="q4_option4" name="q4" value="4">
            <label for="q4_option4">SWOT分析</label>
        </form>
        <p class="result" id="result4"></p>
        <p class="explanation" id="explanation4">
            解説: サービス品質の向上に使用されるモデルとして、狩野モデルがあります。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q4', 1, 'result4', 'explanation4')">
    </div>

    <!-- 問題5 -->
    <div class="question-container" id="question5">
        <p>顧客満足に対する論理的満足の例として正しいものはどれですか？</p>
        <form>
            <input type="radio" id="q5_option1" name="q5" value="1">
            <label for="q5_option1">商品のデザインが魅力的な場合</label><br>
            <input type="radio" id="q5_option2" name="q5" value="2">
            <label for="q5_option2">安価な価格で購入した時</label><br>
            <input type="radio" id="q5_option3" name="q5" value="3">
            <label for="q5_option3">感情的なブランド愛着を持つ場合</label><br>
            <input type="radio" id="q5_option4" name="q5" value="4">
            <label for="q5_option4">サービスの効率が高い場合</label>
        </form>
        <p class="result" id="result5"></p>
        <p class="explanation" id="explanation5">
            解説: 論理的満足としては、安価な価格で商品を購入できた場合が該当します。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q5', 2, 'result5', 'explanation5')">
    </div>

    <!-- 問題6 -->
    <div class="question-container" id="question6">
        <p>どの品質が顧客にとって当たり前の品質であり、不満足の原因となる可能性が高いですか？</p>
        <form>
            <input type="radio" id="q6_option1" name="q6" value="1">
            <label for="q6_option1">一元的品質</label><br>
            <input type="radio" id="q6_option2" name="q6" value="2">
            <label for="q6_option2">魅力的品質</label><br>
            <input type="radio" id="q6_option3" name="q6" value="3">
            <label for="q6_option3">当たり前品質</label><br>
            <input type="radio" id="q6_option4" name="q6" value="4">
            <label for="q6_option4">特別品質</label>
        </form>
        <p class="result" id="result6"></p>
        <p class="explanation" id="explanation6">
            解説: 当たり前品質とは、顧客にとってあって当たり前の基本的な品質であり、この品質が満たされていないと顧客は不満に感じる可能性が高いです。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q6', 3, 'result6', 'explanation6')">
    </div>

    <!-- 問題7 -->
    <div class="question-container" id="question7">
        <p>顧客満足に対する感情的満足の例として正しいものはどれですか？</p>
        <form>
            <input type="radio" id="q7_option1" name="q7" value="1">
            <label for="q7_option1">商品の機能性が高い場合</label><br>
            <input type="radio" id="q7_option2" name="q7" value="2">
            <label for="q7_option2">ブランドに対する信頼感がある場合</label><br>
            <input type="radio" id="q7_option3" name="q7" value="3">
            <label for="q7_option3">安価な価格で購入した時</label><br>
            <input type="radio" id="q7_option4" name="q7" value="4">
            <label for="q7_option4">自分の好みに合ったデザインの商品を購入した時</label>
        </form>
        <p class="result" id="result7"></p>
        <p class="explanation" id="explanation7">
            解説: 感情的満足としては、ブランドに対する信頼感や愛着がある場合が該当します。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q7', 2, 'result7', 'explanation7')">
    </div>

    <!-- 問題8 -->
    <div class="question-container" id="question8">
        <p>サービス品質を改善するために使用されるモデルは次のうちどれですか？</p>
        <form>
            <input type="radio" id="q8_option1" name="q8" value="1">
            <label for="q8_option1">狩野モデル</label><br>
            <input type="radio" id="q8_option2" name="q8" value="2">
            <label for="q8_option2">マーケティングミックス</label><br>
            <input type="radio" id="q8_option3" name="q8" value="3">
            <label for="q8_option3">BCGマトリックス</label><br>
            <input type="radio" id="q8_option4" name="q8" value="4">
            <label for="q8_option4">SWOT分析</label>
        </form>
        <p class="result" id="result8"></p>
        <p class="explanation" id="explanation8">
            解説: サービス品質の改善に使用されるモデルとして、狩野モデルが選ばれます。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q8', 1, 'result8', 'explanation8')">
    </div>

    <!-- 問題9 -->
    <div class="question-container" id="question9">
        <p>顧客にとって重要な要素として正しいものはどれですか？</p>
        <form>
            <input type="radio" id="q9_option1" name="q9" value="1">
            <label for="q9_option1">安価な価格</label><br>
            <input type="radio" id="q9_option2" name="q9" value="2">
            <label for="q9_option2">サービスの多様性</label><br>
            <input type="radio" id="q9_option3" name="q9" value="3">
            <label for="q9_option3">高品質なサービス</label><br>
            <input type="radio" id="q9_option4" name="q9" value="4">
            <label for="q9_option4">早いサービスの提供</label>
        </form>
        <p class="result" id="result9"></p>
        <p class="explanation" id="explanation9">
            解説: 顧客満足において重要な要素として、高品質なサービスが挙げられます。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q9', 3, 'result9', 'explanation9')">
    </div>

    <!-- 問題10 -->
    <div class="question-container" id="question10">
        <p>顧客満足に対する魅力的品質の例として正しいものはどれですか？</p>
        <form>
            <input type="radio" id="q10_option1" name="q10" value="1">
            <label for="q10_option1">サービスの迅速さ</label><br>
            <input type="radio" id="q10_option2" name="q10" value="2">
            <label for="q10_option2">基本的なサービス品質</label><br>
            <input type="radio" id="q10_option3" name="q10" value="3">
            <label for="q10_option3">当たり前品質</label><br>
            <input type="radio" id="q10_option4" name="q10" value="4">
            <label for="q10_option4">特別品質</label>
        </form>
        <p class="result" id="result10"></p>
        <p class="explanation" id="explanation10">
            解説: 魅力的品質としては、顧客が特に価値を感じる追加の品質や特徴が含まれます。
        </p>
        <input type="button" value="回答" onclick="checkAnswer('q10', 4, 'result10', 'explanation10')">
    </div>

    <script>
        function checkAnswer(questionId, correctOption, resultId, explanationId) {
            const radios = document.getElementsByName(questionId);
            let selectedValue;
            for (const radio of radios) {
                if (radio.checked) {
                    selectedValue = radio.value;
                    break;
                }
            }

            const result = document.getElementById(resultId);
            const explanation = document.getElementById(explanationId);
            if (selectedValue == correctOption) {
                result.textContent = '正解です！';
                result.classList.add('correct');
            } else {
                result.textContent = '不正解です。正解は「' + document.querySelector('label[for=' + questionId + '_option' + correctOption + ']').textContent + '」です。';
                result.classList.add('incorrect');
            }
            explanation.style.display = 'block';
        }
    </script>
</body>
</html>
