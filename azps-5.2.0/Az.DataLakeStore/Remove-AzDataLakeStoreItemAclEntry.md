---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: b6d07dbf390a0835bd28a045e4eea8bcf29e15f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330101"
---
# <span data-ttu-id="bba89-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bba89-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="bba89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba89-102">SYNOPSIS</span></span>
<span data-ttu-id="bba89-103">Eltávolít egy bejegyzést a Data Lake Store-beli fájlok vagy mappák ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="bba89-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bba89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bba89-104">SYNTAX</span></span>

### <span data-ttu-id="bba89-105">RemoveByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bba89-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bba89-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="bba89-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba89-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bba89-107">DESCRIPTION</span></span>
<span data-ttu-id="bba89-108">A **Remove-AzDataLakeStoreItemAclEntry** parancsmag eltávolít egy bejegyzést (ACE) a Data Lake Store-beli fájlok vagy mappák hozzáférés-vezérlési listájából.</span><span class="sxs-lookup"><span data-stu-id="bba89-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bba89-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bba89-109">EXAMPLES</span></span>

### <span data-ttu-id="bba89-110">1. példa: Felhasználói bejegyzés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bba89-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="bba89-111">Ez a parancs eltávolítja a Patti Fuller-felhasználó ACE-ét a ContosoADL-fiókból.</span><span class="sxs-lookup"><span data-stu-id="bba89-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="bba89-112">2. példa: Felhasználó bejegyzésének eltávolítása rekurzív módon</span><span class="sxs-lookup"><span data-stu-id="bba89-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="bba89-113">3. példa: Acl-objektum használatával rekurzív ACE-engedélyek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bba89-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="bba89-114">Ez a parancs eltávolítja a Patti Fuller-hez szükséges felhasználói ACE-t a legfelső szintűről, és rekurzívan törli a ContosoADL-fiókhoz szükséges alkönyvtárakat és fájlokat.</span><span class="sxs-lookup"><span data-stu-id="bba89-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="bba89-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bba89-115">PARAMETERS</span></span>

### <span data-ttu-id="bba89-116">-Account</span><span class="sxs-lookup"><span data-stu-id="bba89-116">-Account</span></span>
<span data-ttu-id="bba89-117">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bba89-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="bba89-118">-AceType</span></span>
<span data-ttu-id="bba89-119">Az eltávolítható ACE típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="bba89-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="bba89-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="bba89-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bba89-121">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="bba89-121">User</span></span>
- <span data-ttu-id="bba89-122">Csoportosítás</span><span class="sxs-lookup"><span data-stu-id="bba89-122">Group</span></span>
- <span data-ttu-id="bba89-123">Maszk</span><span class="sxs-lookup"><span data-stu-id="bba89-123">Mask</span></span>
- <span data-ttu-id="bba89-124">Egyéb</span><span class="sxs-lookup"><span data-stu-id="bba89-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="bba89-125">-Acl</span></span>
<span data-ttu-id="bba89-126">Az eltávolítható bejegyzéseket tartalmazó ACL-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bba89-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-127">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="bba89-127">-Concurrency</span></span>
<span data-ttu-id="bba89-128">A párhuzamosan feldolgozott fájlok és könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="bba89-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="bba89-129">Nem kötelező: egy észszerű alapértelmezett beállítás lesz kiválasztva</span><span class="sxs-lookup"><span data-stu-id="bba89-129">Optional: a reasonable default will be selected</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-130">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="bba89-130">-Default</span></span>
<span data-ttu-id="bba89-131">Azt jelzi, hogy ez a művelet eltávolítja az alapértelmezett ACE-t a megadott ACL-ről.</span><span class="sxs-lookup"><span data-stu-id="bba89-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba89-132">-DefaultProfile</span></span>
<span data-ttu-id="bba89-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bba89-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-134">-Id</span><span class="sxs-lookup"><span data-stu-id="bba89-134">-Id</span></span>
<span data-ttu-id="bba89-135">Annak az AzureActive Directory-felhasználónak, -csoportnak vagy szolgáltatásnévnek az objektumazonosítóját adja meg, amelyről el szeretné távolítani az ACE-et.</span><span class="sxs-lookup"><span data-stu-id="bba89-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bba89-136">-PassThru</span></span>
<span data-ttu-id="bba89-137">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="bba89-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-138">-Path</span><span class="sxs-lookup"><span data-stu-id="bba89-138">-Path</span></span>
<span data-ttu-id="bba89-139">Annak az elemnek a Data Lake Store-elérési útját adja meg, amelyből el szeretné távolítani az ACE-t, a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="bba89-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="bba89-140">-Recurse</span></span>
<span data-ttu-id="bba89-141">Azt jelzi, hogy az ACL-et rekurzív módon el kell távolítani a gyermek alkönyvtáraiból és fájljaiból.</span><span class="sxs-lookup"><span data-stu-id="bba89-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="bba89-142">-ShowProgress</span></span>
<span data-ttu-id="bba89-143">Ha a folyamat elért, akkor a folyamat állapota 2010-et mutat.</span><span class="sxs-lookup"><span data-stu-id="bba89-143">If passed then progress status is showed.</span></span> <span data-ttu-id="bba89-144">Csak akkor alkalmazható, ha a rekurzív Acl eltávolítás kész.</span><span class="sxs-lookup"><span data-stu-id="bba89-144">Only applicable when recursive Acl remove is done.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bba89-145">-Confirm</span></span>
<span data-ttu-id="bba89-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bba89-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba89-147">-WhatIf</span></span>
<span data-ttu-id="bba89-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bba89-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba89-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bba89-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba89-150">CommonParameters</span></span>
<span data-ttu-id="bba89-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba89-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba89-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba89-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba89-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bba89-153">INPUTS</span></span>

### <span data-ttu-id="bba89-154">System.String</span><span class="sxs-lookup"><span data-stu-id="bba89-154">System.String</span></span>

### <span data-ttu-id="bba89-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="bba89-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bba89-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="bba89-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="bba89-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="bba89-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="bba89-158">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bba89-158">System.Guid</span></span>

### <span data-ttu-id="bba89-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bba89-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bba89-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bba89-160">System.Int32</span></span>

## <span data-ttu-id="bba89-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bba89-161">OUTPUTS</span></span>

### <span data-ttu-id="bba89-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bba89-162">System.Boolean</span></span>

## <span data-ttu-id="bba89-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bba89-163">NOTES</span></span>

## <span data-ttu-id="bba89-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bba89-164">RELATED LINKS</span></span>

[<span data-ttu-id="bba89-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bba89-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


