# GoMyCode-Data-Structures-Checkpoint

# Algorithm for Q1
Algorithm distinct_sum(set1, set2)
    Initialize empty array distinct_elements
    Initialize variable sum = 0
    
    for each element in set1 do
        if element is not in set2 and element is not in distinct_elements then
            add element to distinct_elements
            add element to sum
        end if
    end for
    
    for each element in set2 do
        if element is not in set1 and element is not in distinct_elements then
            add element to distinct_elements
            add element to sum
        end if
    end for
    
    return sum
End Algorithm


# JavaScript Code for Q1
function distinctSum(set1, set2) {
  const distinctElements = [];
  let sum = 0;

  for (let i = 0; i < set1.length; i++) {
    if (!set2.includes(set1[i]) && !distinctElements.includes(set1[i])) {
      distinctElements.push(set1[i]);
      sum += set1[i];
    }
  }

  for (let i = 0; i < set2.length; i++) {
    if (!set1.includes(set2[i]) && !distinctElements.includes(set2[i])) {
      distinctElements.push(set2[i]);
      sum += set2[i];
    }
  }

  return sum;
}



# Algorithm for Q2
    Procedure dot_product(v1, v2):
    a. Initialize ps = 0.
    b. For i = 0 to n-1:
    i. ps += v1[i] * v2[i]
    c. Return ps

    Algorithm check_orthogonality(n, v):
    a. For i = 0 to n-1:
    i. For j = i+1 to n-1:
    1. ps = dot_product(v[i], v[j])
    2. If ps == 0, print "Vector i and vector j are orthogonal"
    3. Else, print "Vector i and vector j are not orthogonal"

    Function dotProduct(v1, v2):
    a. Initialize ps = 0.
    b. For i = 0 to n-1:
    i. ps += v1[i] * v2[i]
    c. Return ps

    Algorithm checkOrthogonality(n, v):
    a. For i = 0 to n-1:
    i. For j = i+1 to n-1:
    1. ps = dotProduct(v[i], v[j])
    2. If ps == 0, print "Vector i and vector j are orthogonal"
    3. Else, print "Vector i and vector j are not orthogonal"
    
    Description:

    The procedure dot_product takes in two vectors v1 and v2 of IR and calculates their dot product by iterating over the elements of the vectors and multiplying the corresponding elements together and summing them up.

    The algorithm check_orthogonality takes in the number of pairs of vectors n and an array of vectors v. It calls the dot_product procedure for each pair of vectors and checks if the dot product is zero or not. If the dot product is zero, then it prints that the vectors are orthogonal, otherwise it prints that they are not orthogonal.

    The function dotProduct is similar to the dot_product procedure, but it returns the dot product instead of storing it in a variable.

    The algorithm checkOrthogonality is similar to check_orthogonality, but it calls the dotProduct function instead of the dot_product procedure.


# JavaScript Code for Q2
// Procedure dot_product
function dot_product(v1, v2) {
  let ps = 0;
  for (let i = 0; i < v1.length; i++) {
    ps += v1[i] * v2[i];
  }
  return ps;
}

// Algorithm check_orthogonality
function check_orthogonality(n, v) {
  for (let i = 0; i < n; i++) {
    for (let j = i + 1; j < n; j++) {
      const ps = dot_product(v[i], v[j]);
      if (ps === 0) {
        console.log(`Vector ${i} and vector ${j} are orthogonal`);
      } else {
        console.log(`Vector ${i} and vector ${j} are not orthogonal`);
      }
    }
  }
}

// Function dotProduct
function dotProduct(v1, v2) {
  let ps = 0;
  for (let i = 0; i < v1.length; i++) {
    ps += v1[i] * v2[i];
  }
  return ps;
}

// Algorithm checkOrthogonality
function checkOrthogonality(n, v) {
  for (let i = 0; i < n; i++) {
    for (let j = i + 1; j < n; j++) {
      const ps = dotProduct(v[i], v[j]);
      if (ps === 0) {
        console.log(`Vector ${i} and vector ${j} are orthogonal`);
      } else {
        console.log(`Vector ${i} and vector ${j} are not orthogonal`);
      }
    }
  }
}
