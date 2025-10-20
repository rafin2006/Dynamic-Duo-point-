<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DYNAMIC DUO POINT CALCULATOR</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Hind+Siliguri:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', 'Hind Siliguri', sans-serif;
        }
        .result-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .penalty {
            color: #ef4444; /* red-500 */
        }
        .bonus {
            color: #22c55e; /* green-500 */
        }
        .final-score {
            font-size: 2.5rem;
            font-weight: 700;
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-100 min-h-screen flex items-center justify-center p-4">
    <div class="w-full max-w-2xl mx-auto">
        <div class="bg-gray-800 shadow-2xl rounded-2xl p-6 md:p-10">
            <div class="text-center mb-8">
                <h1 class="text-3xl md:text-4xl font-bold text-white">DYNAMIC DUO POINT CALCULATOR</h1>
                <p class="text-gray-400 mt-2">Enter your team's hours to calculate the final score.</p>
            </div>

            <form id="calculatorForm" class="space-y-6">
                <div>
                    <label for="session" class="block text-sm font-medium text-gray-300 mb-2">Select Session</label>
                    <select id="session" name="session" class="w-full bg-gray-700 border border-gray-600 text-white rounded-lg p-3 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 transition">
                        <option value="morning">🌅 Morning Session (5 AM – 1 PM)</option>
                        <option value="noon">☀️ Noon Session (1 PM – 6 PM)</option>
                        <option value="evening">🌙 Evening Session (6 PM – 5 AM)</option>
                    </select>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label for="member1_hours" class="block text-sm font-medium text-gray-300 mb-2">Member 1: Hours Studied</label>
                        <input type="number" step="0.01" id="member1_hours" name="member1_hours" class="w-full bg-gray-700 border border-gray-600 text-white rounded-lg p-3 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 transition" placeholder="e.g., 4.5" required>
                    </div>
                    <div>
                        <label for="member2_hours" class="block text-sm font-medium text-gray-300 mb-2">Member 2: Hours Studied</label>
                        <input type="number" step="0.01" id="member2_hours" name="member2_hours" class="w-full bg-gray-700 border border-gray-600 text-white rounded-lg p-3 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 transition" placeholder="e.g., 3.75" required>
                    </div>
                </div>
                
                <div class="border-t border-gray-700 pt-6">
                     <p class="text-sm font-medium text-gray-300 mb-4">Late Submission (if applicable)</p>
                     <div class="flex items-center space-x-8">
                         <div class="relative flex items-start">
                            <div class="flex items-center h-5">
                                <input id="late_submission" name="late_submission" type="checkbox" class="focus:ring-indigo-500 h-4 w-4 text-indigo-600 bg-gray-700 border-gray-600 rounded">
                            </div>
                            <div class="ml-3 text-sm">
                                <label for="late_submission" class="font-medium text-gray-300">Did anyone on the team submit late?</label>
                            </div>
                        </div>
                     </div>
                </div>

                <div>
                    <button type="submit" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-4 rounded-lg text-lg transition duration-300 ease-in-out transform hover:scale-105">
                        Calculate Score
                    </button>
                </div>
            </form>

            <div id="results" class="mt-10 hidden">
                 <h2 class="text-2xl font-bold text-center mb-6">Score Breakdown</h2>
                 <div class="bg-gray-800 rounded-lg p-6 border border-gray-700">
                    <div id="breakdown-list" class="space-y-3 text-lg">
                        <!-- Calculation details will be injected here -->
                    </div>
                    <div class="border-t-2 border-dashed border-gray-600 my-4"></div>
                    <div class="text-center">
                         <p class="text-gray-400 font-medium">Final Team Score</p>
                         <p id="final-score" class="final-score text-indigo-400">0</p>
                    </div>
                 </div>
            </div>
        </div>
    </div>

    <script>
        const form = document.getElementById('calculatorForm');
        const resultsDiv = document.getElementById('results');
        const breakdownList = document.getElementById('breakdown-list');
        const finalScoreEl = document.getElementById('final-score');

        form.addEventListener('submit', function(e) {
            e.preventDefault();

            // --- Get Inputs ---
            const session = document.getElementById('session').value;
            const hours1 = parseFloat(document.getElementById('member1_hours').value) || 0;
            const hours2 = parseFloat(document.getElementById('member2_hours').value) || 0;
            const isLate = document.getElementById('late_submission').checked;

            // --- Rule Definitions ---
            let pointsPerHour = 1;
            let targetHours = 0;

            if (session === 'morning' || session === 'evening') {
                pointsPerHour = 2;
                targetHours = 4;
            }

            // --- Initial Calculations ---
            let breakdownHTML = '';
            let penalties = [];
            
            // Rule 1: Calculate only full hours
            const fullHours1 = Math.floor(hours1);
            const fullHours2 = Math.floor(hours2);

            let points1 = 0;
            let bonus1 = 0;
            let points2 = 0;
            let bonus2 = 0;
            
            // Rule: No points if target is not met
            if(session !== 'noon'){
                if (fullHours1 >= targetHours) {
                    points1 = targetHours * pointsPerHour;
                    bonus1 = (fullHours1 - targetHours);
                }
                if (fullHours2 >= targetHours) {
                    points2 = targetHours * pointsPerHour;
                    bonus2 = (fullHours2 - targetHours);
                }
            } else { // Noon session has no target
                points1 = fullHours1 * pointsPerHour;
                points2 = fullHours2 * pointsPerHour;
            }
            
            let initialPoints = points1 + bonus1 + points2 + bonus2;
            let totalScore = initialPoints;

            // --- Display Earned Points ---
            breakdownHTML += `<div class="result-item"><span>Member 1 (${fullHours1} hrs):</span><span class="font-semibold">${points1 + bonus1} pts</span></div>`;
            if (bonus1 > 0) breakdownHTML += `<div class="result-item text-sm pl-4"><span>└ Member 1 Bonus:</span><span class="font-semibold bonus">+${bonus1}</span></div>`;
            breakdownHTML += `<div class="result-item"><span>Member 2 (${fullHours2} hrs):</span><span class="font-semibold">${points2 + bonus2} pts</span></div>`;
            if (bonus2 > 0) breakdownHTML += `<div class="result-item text-sm pl-4"><span>└ Member 2 Bonus:</span><span class="font-semibold bonus">+${bonus2}</span></div>`;
            breakdownHTML += `<div class="result-item border-t border-gray-700 pt-2 mt-2"><strong>Initial Team Total:</strong><strong>${initialPoints} pts</strong></div>`;
            
            // --- Penalty Calculations ---
            
            // Rule 2: Late submission penalty
            if (isLate) {
                totalScore -= 2;
                // Late submission cancels any bonus points
                if(bonus1 > 0) totalScore -= bonus1;
                if(bonus2 > 0) totalScore -= bonus2;
                penalties.push({ text: "Late Submission", value: -2 });
            }

            // Rule 3: Target failure penalty (only for Morning/Evening)
            if (session !== 'noon') {
                const failed1 = fullHours1 < targetHours;
                const failed2 = fullHours2 < targetHours;

                if (failed1 && failed2) {
                    totalScore -= 4;
                    penalties.push({ text: "Both failed target", value: -4 });
                } else if (failed1 || failed2) {
                    totalScore -= 2;
                    const failedMember = failed1 ? "Member 1" : "Member 2";
                    penalties.push({ text: `${failedMember} failed target`, value: -2 });
                }
            }
            
            // --- Finalize and Display ---
            if (totalScore < 0) {
                totalScore = 0;
            }

            // Add penalties to the breakdown
            if(penalties.length > 0){
                 breakdownHTML += `<div class="result-item pt-4"><strong class="penalty">Penalties:</strong><span></span></div>`;
                 penalties.forEach(p => {
                     breakdownHTML += `<div class="result-item text-sm pl-4"><span class="penalty">${p.text}</span><span class="font-semibold penalty">${p.value}</span></div>`;
                 });
            }

            breakdownList.innerHTML = breakdownHTML;
            finalScoreEl.textContent = Math.round(totalScore);
            resultsDiv.classList.remove('hidden');
        });
    </script>
</body>
</html>


