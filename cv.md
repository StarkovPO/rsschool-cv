# CV

# Starkov Pavel 
===
### Contact information:
**Phone:** +7 912-58-32-77-1
**E-mail:** straiker666@gmail.com
**Telegram:** p_starkov
===
### About me:

I've started worked in IT company in september 2021 on position Junior QA Engineer. On work I learned Javascript for writing npm testing API after that I've got an ability to writing E2E test via playwright on JS. Now I'm middle QA Automation Engineer, but I wanna programming more that I get now.

My goal is become to fullstack developer on JS, who have skill in FE/BE/Testing. 
===
### Skills:

* Regression testing
* DevTools
* Git
* SQL
* Postman
* Performing Testing via K6
* Mocha/chai
* Playwright
* Javascript
* HTML
* CSS
* Axios
===
### Code example:

```
export const deleteAllUsers = async (token: string, projectId: string) => {
  const getUsers = await axios.get(`https://test-login.xsolla.com/api/projects/${projectId}/users/search`, {
    httpsAgent,
    params: {
      limit: 100,
      order_dir: 'asc',
      offset: 0,
      order_column: 'username',
    },
    headers: {
      Authorization: `Bearer ${token}`,
    },
  });
  const usersList = getUsers.data.users.map(user => {
    return user.id;
  });
  const deleteUser = async (userId: string) => {
    return axios.delete(`https://test-login.xsolla.com/api/users/${userId}`, {
      httpsAgent,
      params: {
        projectId,
      },
      headers: {
        Authorization: `Bearer ${token}`,
      },
    });
  };
  await asyncForEach(usersList, async (userId: string) => {
    await deleteUser(userId);
    console.log('User deleted', userId);
    await awaitTimeout(2000);
  });

  return 1;
};
```
===
### Experience:
1. Junior QA Engineer October 2021 - September 2022 Xsolla
2. Middle QA Automation Engineer September 2022 - now Xsolla
===
### Education:
**University:** PSTU, Math Modeling 2022, Bachelor of Applied Mathematics and Informatics
**Courses:** 
1. OTUS QA Automation Engineer Javascript
2. Agile/Scrum Xsolla
3. Manual QA Xsolla external course
4. Docker Beginner
===
### Languages:
- English:  B1
- Russian:  C2