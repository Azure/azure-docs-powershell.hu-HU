---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 7cc09813f03e5424b7d44b7a56810167ca5affba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671056"
---
# <span data-ttu-id="31014-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31014-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="31014-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31014-102">SYNOPSIS</span></span>
<span data-ttu-id="31014-103">Az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének a bejegyzését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="31014-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="31014-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31014-104">SYNTAX</span></span>

### <span data-ttu-id="31014-105">RemoveByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31014-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31014-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="31014-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31014-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="31014-107">DESCRIPTION</span></span>
<span data-ttu-id="31014-108">A **Remove-AzDataLakeStoreItemAclEntry** parancsmag az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában található bejegyzés (ACE) eltávolítását távolítja el.</span><span class="sxs-lookup"><span data-stu-id="31014-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="31014-109">Példák</span><span class="sxs-lookup"><span data-stu-id="31014-109">EXAMPLES</span></span>

### <span data-ttu-id="31014-110">Példa 1: felhasználó bejegyzésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="31014-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="31014-111">Ez a parancs eltávolítja a felhasználó ACE for Patti Fuller-t az ContosoADL-fiókból.</span><span class="sxs-lookup"><span data-stu-id="31014-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="31014-112">2. példa: felhasználói bejegyzés rekurzív eltávolítása</span><span class="sxs-lookup"><span data-stu-id="31014-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="31014-113">3. példa: az ACE rekurzív engedélyeinek eltávolítása az ACL-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="31014-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="31014-114">Ez a parancs eltávolítja a felhasználó ACE for Patti Fuller-t a root-ből, és rekurzívan a fiók ContosoADL tartozó összes alkönyvtárból és fájlból.</span><span class="sxs-lookup"><span data-stu-id="31014-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="31014-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31014-115">PARAMETERS</span></span>

### <span data-ttu-id="31014-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="31014-116">-Account</span></span>
<span data-ttu-id="31014-117">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31014-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="31014-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="31014-118">-AceType</span></span>
<span data-ttu-id="31014-119">Az eltávolítandó ACE típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="31014-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="31014-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="31014-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31014-121">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="31014-121">User</span></span>
- <span data-ttu-id="31014-122">Csoport</span><span class="sxs-lookup"><span data-stu-id="31014-122">Group</span></span>
- <span data-ttu-id="31014-123">Maszk</span><span class="sxs-lookup"><span data-stu-id="31014-123">Mask</span></span>
- <span data-ttu-id="31014-124">Más</span><span class="sxs-lookup"><span data-stu-id="31014-124">Other</span></span>

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

### <span data-ttu-id="31014-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="31014-125">-Acl</span></span>
<span data-ttu-id="31014-126">Megadja az eltávolítandó bejegyzéseket tartalmazó ACL-objektumot.</span><span class="sxs-lookup"><span data-stu-id="31014-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="31014-127">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="31014-127">-Concurrency</span></span>
<span data-ttu-id="31014-128">A párhuzamosan feldolgozott fájlok/könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="31014-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="31014-129">Nem kötelező: a program megfelelő alapértelmezett beállítást ad meg.</span><span class="sxs-lookup"><span data-stu-id="31014-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="31014-130">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="31014-130">-Default</span></span>
<span data-ttu-id="31014-131">Azt jelzi, hogy ez a művelet eltávolítja az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="31014-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="31014-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31014-132">-DefaultProfile</span></span>
<span data-ttu-id="31014-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31014-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31014-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="31014-134">-Id</span></span>
<span data-ttu-id="31014-135">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelyből egy ÁSZT el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="31014-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="31014-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31014-136">-PassThru</span></span>
<span data-ttu-id="31014-137">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="31014-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="31014-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="31014-138">-Path</span></span>
<span data-ttu-id="31014-139">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyből el szeretné távolítani az ÁSZT (/) a gyökérkönyvtártól kezdve.</span><span class="sxs-lookup"><span data-stu-id="31014-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="31014-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="31014-140">-Recurse</span></span>
<span data-ttu-id="31014-141">Azt jelzi, hogy a rendszer rekurzív módon távolítja el a alárendelt alkönyvtárakat és fájlokat</span><span class="sxs-lookup"><span data-stu-id="31014-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="31014-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="31014-142">-ShowProgress</span></span>
<span data-ttu-id="31014-143">Ha a betelt, akkor a folyamat állapota látható.</span><span class="sxs-lookup"><span data-stu-id="31014-143">If passed then progress status is showed.</span></span> <span data-ttu-id="31014-144">Csak akkor érvényes, ha a rekurzív ACL-eltávolítás befejeződött.</span><span class="sxs-lookup"><span data-stu-id="31014-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="31014-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31014-145">-Confirm</span></span>
<span data-ttu-id="31014-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31014-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31014-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31014-147">-WhatIf</span></span>
<span data-ttu-id="31014-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31014-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31014-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31014-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31014-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31014-150">CommonParameters</span></span>
<span data-ttu-id="31014-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31014-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31014-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31014-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31014-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31014-153">INPUTS</span></span>

### <span data-ttu-id="31014-154">System. String</span><span class="sxs-lookup"><span data-stu-id="31014-154">System.String</span></span>

### <span data-ttu-id="31014-155">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="31014-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="31014-156">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="31014-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="31014-157">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="31014-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="31014-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="31014-158">System.Guid</span></span>

### <span data-ttu-id="31014-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31014-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="31014-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="31014-160">System.Int32</span></span>

## <span data-ttu-id="31014-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31014-161">OUTPUTS</span></span>

### <span data-ttu-id="31014-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31014-162">System.Boolean</span></span>

## <span data-ttu-id="31014-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31014-163">NOTES</span></span>

## <span data-ttu-id="31014-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31014-164">RELATED LINKS</span></span>

[<span data-ttu-id="31014-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31014-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


