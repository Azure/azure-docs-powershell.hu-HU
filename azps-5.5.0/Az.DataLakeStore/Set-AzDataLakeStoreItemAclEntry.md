---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161866"
---
# <span data-ttu-id="66e9e-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="66e9e-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="66e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="66e9e-103">Módosít egy bejegyzést a Data Lake Store-beli fájlok vagy mappák ACL-ében.</span><span class="sxs-lookup"><span data-stu-id="66e9e-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="66e9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66e9e-104">SYNTAX</span></span>

### <span data-ttu-id="66e9e-105">SetByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66e9e-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66e9e-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="66e9e-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66e9e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66e9e-107">DESCRIPTION</span></span>
<span data-ttu-id="66e9e-108">A **Set-AzDataLakeStoreItemAclEntry** parancsmag módosítja a Data Lake Store-beli fájlok vagy mappák hozzáférés-vezérlési listájában (ACE) szereplő bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="66e9e-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="66e9e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66e9e-109">EXAMPLES</span></span>

### <span data-ttu-id="66e9e-110">1. példa: Hozzáférési hozzáférési engedély engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="66e9e-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="66e9e-111">Ez a parancs módosítja a Patti Fuller-hez szükséges ACE-t, hogy minden engedéllyel rendelkeznie kell.</span><span class="sxs-lookup"><span data-stu-id="66e9e-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="66e9e-112">2. példa: AZ ACE-rekurzív engedélyek módosítása</span><span class="sxs-lookup"><span data-stu-id="66e9e-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="66e9e-113">3. példa: Hozzáférési hozzáférési jogosultságok rekurzív módosítása Acl-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="66e9e-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="66e9e-114">Ez a parancs rekurzív módon módosítja a Patti Fuller-hez szükséges ACE-t, hogy minden engedélyével rendelkeznie kell a roothoz, valamint az alkönyvtárakhoz és fájlokhoz.</span><span class="sxs-lookup"><span data-stu-id="66e9e-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="66e9e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66e9e-115">PARAMETERS</span></span>

### <span data-ttu-id="66e9e-116">-Account</span><span class="sxs-lookup"><span data-stu-id="66e9e-116">-Account</span></span>
<span data-ttu-id="66e9e-117">Az Adattavatár-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66e9e-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="66e9e-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="66e9e-118">-AceType</span></span>
<span data-ttu-id="66e9e-119">A módosítani szükséges ACE-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="66e9e-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="66e9e-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="66e9e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66e9e-121">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="66e9e-121">User</span></span> 
- <span data-ttu-id="66e9e-122">Csoportosítás</span><span class="sxs-lookup"><span data-stu-id="66e9e-122">Group</span></span> 
- <span data-ttu-id="66e9e-123">Maszk</span><span class="sxs-lookup"><span data-stu-id="66e9e-123">Mask</span></span> 
- <span data-ttu-id="66e9e-124">Egyéb</span><span class="sxs-lookup"><span data-stu-id="66e9e-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e9e-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="66e9e-125">-Acl</span></span>
<span data-ttu-id="66e9e-126">A módosítani kívánt bejegyzéseket tartalmazó ACL-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="66e9e-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e9e-127">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="66e9e-127">-Concurrency</span></span>
<span data-ttu-id="66e9e-128">A párhuzamosan feldolgozott fájlok és könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="66e9e-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="66e9e-129">Nem kötelező: egy észszerű alapértelmezett beállítás lesz kiválasztva</span><span class="sxs-lookup"><span data-stu-id="66e9e-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="66e9e-130">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="66e9e-130">-Default</span></span>
<span data-ttu-id="66e9e-131">Azt jelzi, hogy ez a művelet módosítja az alapértelmezett ACE-t a megadott ACL-től.</span><span class="sxs-lookup"><span data-stu-id="66e9e-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e9e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e9e-132">-DefaultProfile</span></span>
<span data-ttu-id="66e9e-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66e9e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66e9e-134">-Id</span><span class="sxs-lookup"><span data-stu-id="66e9e-134">-Id</span></span>
<span data-ttu-id="66e9e-135">Annak az AzureActive Directory-felhasználónak, -csoportnak vagy szolgáltatásnévnek az objektumazonosítóját adja meg, amelynek módosítania kell egy ACE-et.</span><span class="sxs-lookup"><span data-stu-id="66e9e-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e9e-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66e9e-136">-PassThru</span></span>
<span data-ttu-id="66e9e-137">Azt jelzi, hogy az eredményül kapott ACL-t kell eredményül visszaadni.</span><span class="sxs-lookup"><span data-stu-id="66e9e-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="66e9e-138">-Path</span><span class="sxs-lookup"><span data-stu-id="66e9e-138">-Path</span></span>
<span data-ttu-id="66e9e-139">Annak az elemnek a Data Lake Store-elérési útját adja meg, amelynek módosítani szeretné az ACE-t a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="66e9e-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="66e9e-140">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="66e9e-140">-Permissions</span></span>
<span data-ttu-id="66e9e-141">Az ACE engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="66e9e-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="66e9e-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="66e9e-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66e9e-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="66e9e-143">None</span></span>
- <span data-ttu-id="66e9e-144">Execute</span><span class="sxs-lookup"><span data-stu-id="66e9e-144">Execute</span></span>
- <span data-ttu-id="66e9e-145">Írás</span><span class="sxs-lookup"><span data-stu-id="66e9e-145">Write</span></span>
- <span data-ttu-id="66e9e-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="66e9e-146">WriteExecute</span></span>
- <span data-ttu-id="66e9e-147">Olvasás</span><span class="sxs-lookup"><span data-stu-id="66e9e-147">Read</span></span>
- <span data-ttu-id="66e9e-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="66e9e-148">ReadExecute</span></span>
- <span data-ttu-id="66e9e-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="66e9e-149">ReadWrite</span></span>
- <span data-ttu-id="66e9e-150">Mind</span><span class="sxs-lookup"><span data-stu-id="66e9e-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e9e-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="66e9e-151">-Recurse</span></span>
<span data-ttu-id="66e9e-152">Azt jelzi, hogy az ACL-t rekurzíven módosítani kell a gyermek alkönyvtárai és fájljai számára.</span><span class="sxs-lookup"><span data-stu-id="66e9e-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="66e9e-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="66e9e-153">-ShowProgress</span></span>
<span data-ttu-id="66e9e-154">Ha a folyamat elért, akkor a folyamat állapota 2010-et mutat.</span><span class="sxs-lookup"><span data-stu-id="66e9e-154">If passed then progress status is showed.</span></span> <span data-ttu-id="66e9e-155">Csak akkor alkalmazható, ha a rekurzív Acl módosítás történik.</span><span class="sxs-lookup"><span data-stu-id="66e9e-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="66e9e-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66e9e-156">-Confirm</span></span>
<span data-ttu-id="66e9e-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="66e9e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66e9e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e9e-158">-WhatIf</span></span>
<span data-ttu-id="66e9e-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="66e9e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66e9e-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66e9e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66e9e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e9e-161">CommonParameters</span></span>
<span data-ttu-id="66e9e-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e9e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e9e-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66e9e-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e9e-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66e9e-164">INPUTS</span></span>

### <span data-ttu-id="66e9e-165">System.String</span><span class="sxs-lookup"><span data-stu-id="66e9e-165">System.String</span></span>

### <span data-ttu-id="66e9e-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="66e9e-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="66e9e-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="66e9e-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="66e9e-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="66e9e-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="66e9e-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="66e9e-169">System.Guid</span></span>

### <span data-ttu-id="66e9e-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="66e9e-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="66e9e-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66e9e-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="66e9e-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="66e9e-172">System.Int32</span></span>

## <span data-ttu-id="66e9e-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66e9e-173">OUTPUTS</span></span>

### <span data-ttu-id="66e9e-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="66e9e-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="66e9e-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66e9e-175">NOTES</span></span>

## <span data-ttu-id="66e9e-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66e9e-176">RELATED LINKS</span></span>

[<span data-ttu-id="66e9e-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="66e9e-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


