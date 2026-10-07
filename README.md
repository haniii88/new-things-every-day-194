function dailyLog194() {
  const commits = [
    { author: "Alex", count: 5 },
    { author: "Sam", count: 3 },
    { author: "Jordan", count: 7 },
    { author: "Taylor", count: 4 }
  ];

  const totalCommits = commits.reduce(
    (sum, contributor) => sum + contributor.count,
    0
  );

  const topContributor = commits.reduce((top, contributor) =>
    contributor.count > top.count ? contributor : top
  );

  const report = {
    date: new Date().toISOString().split("T")[0],
    totalCommits,
    contributors: commits.length,
    topContributor: topContributor.author,
    topCommitCount: topContributor.count
  };

  console.log("Daily Commit Report:", report);
}

dailyLog194();
