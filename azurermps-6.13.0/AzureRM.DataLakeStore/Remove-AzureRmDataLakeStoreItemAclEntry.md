---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 154c57c6a403fce574a785aaf60d95a7936907b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491940"
---
# <span data-ttu-id="3e612-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3e612-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="3e612-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e612-102">SYNOPSIS</span></span>
<span data-ttu-id="3e612-103">Az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének a bejegyzését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="3e612-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e612-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e612-104">SYNTAX</span></span>

### <span data-ttu-id="3e612-105">RemoveByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e612-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e612-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="3e612-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e612-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e612-107">DESCRIPTION</span></span>
<span data-ttu-id="3e612-108">A **Remove-AzureRmDataLakeStoreItemAclEntry** parancsmag az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában található bejegyzés (ACE) eltávolítását távolítja el.</span><span class="sxs-lookup"><span data-stu-id="3e612-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3e612-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3e612-109">EXAMPLES</span></span>

### <span data-ttu-id="3e612-110">Példa 1: felhasználó bejegyzésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3e612-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="3e612-111">Ez a parancs eltávolítja a felhasználó ACE for Patti Fuller-t az ContosoADL-fiókból.</span><span class="sxs-lookup"><span data-stu-id="3e612-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="3e612-112">2. példa: felhasználói bejegyzés rekurzív eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3e612-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="3e612-113">3. példa: az ACE rekurzív engedélyeinek eltávolítása az ACL-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="3e612-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="3e612-114">Ez a parancs eltávolítja a felhasználó ACE for Patti Fuller-t a root-ből, és rekurzívan a fiók ContosoADL tartozó összes alkönyvtárból és fájlból.</span><span class="sxs-lookup"><span data-stu-id="3e612-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="3e612-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e612-115">PARAMETERS</span></span>

### <span data-ttu-id="3e612-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="3e612-116">-Account</span></span>
<span data-ttu-id="3e612-117">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e612-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3e612-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="3e612-118">-AceType</span></span>
<span data-ttu-id="3e612-119">Az eltávolítandó ACE típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e612-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="3e612-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3e612-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e612-121">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="3e612-121">User</span></span>
- <span data-ttu-id="3e612-122">Csoport</span><span class="sxs-lookup"><span data-stu-id="3e612-122">Group</span></span>
- <span data-ttu-id="3e612-123">Maszk</span><span class="sxs-lookup"><span data-stu-id="3e612-123">Mask</span></span>
- <span data-ttu-id="3e612-124">Más</span><span class="sxs-lookup"><span data-stu-id="3e612-124">Other</span></span>

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

### <span data-ttu-id="3e612-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="3e612-125">-Acl</span></span>
<span data-ttu-id="3e612-126">Megadja az eltávolítandó bejegyzéseket tartalmazó ACL-objektumot.</span><span class="sxs-lookup"><span data-stu-id="3e612-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="3e612-127">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="3e612-127">-Concurrency</span></span>
<span data-ttu-id="3e612-128">A párhuzamosan feldolgozott fájlok/könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="3e612-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="3e612-129">Nem kötelező: a program megfelelő alapértelmezett beállítást ad meg.</span><span class="sxs-lookup"><span data-stu-id="3e612-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="3e612-130">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="3e612-130">-Default</span></span>
<span data-ttu-id="3e612-131">Azt jelzi, hogy ez a művelet eltávolítja az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="3e612-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="3e612-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e612-132">-DefaultProfile</span></span>
<span data-ttu-id="3e612-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e612-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e612-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3e612-134">-Id</span></span>
<span data-ttu-id="3e612-135">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelyből egy ÁSZT el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="3e612-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="3e612-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e612-136">-PassThru</span></span>
<span data-ttu-id="3e612-137">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3e612-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="3e612-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3e612-138">-Path</span></span>
<span data-ttu-id="3e612-139">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyből el szeretné távolítani az ÁSZT (/) a gyökérkönyvtártól kezdve.</span><span class="sxs-lookup"><span data-stu-id="3e612-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3e612-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="3e612-140">-Recurse</span></span>
<span data-ttu-id="3e612-141">Azt jelzi, hogy a rendszer rekurzív módon távolítja el a alárendelt alkönyvtárakat és fájlokat</span><span class="sxs-lookup"><span data-stu-id="3e612-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="3e612-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="3e612-142">-ShowProgress</span></span>
<span data-ttu-id="3e612-143">Ha a betelt, akkor a folyamat állapota látható.</span><span class="sxs-lookup"><span data-stu-id="3e612-143">If passed then progress status is showed.</span></span> <span data-ttu-id="3e612-144">Csak akkor érvényes, ha a rekurzív ACL-eltávolítás befejeződött.</span><span class="sxs-lookup"><span data-stu-id="3e612-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="3e612-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e612-145">-Confirm</span></span>
<span data-ttu-id="3e612-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e612-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e612-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e612-147">-WhatIf</span></span>
<span data-ttu-id="3e612-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e612-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e612-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e612-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e612-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e612-150">CommonParameters</span></span>
<span data-ttu-id="3e612-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e612-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e612-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e612-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e612-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e612-153">INPUTS</span></span>

### <span data-ttu-id="3e612-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3e612-154">System.String</span></span>

### <span data-ttu-id="3e612-155">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3e612-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="3e612-156">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="3e612-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="3e612-157">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="3e612-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="3e612-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3e612-158">System.Guid</span></span>

### <span data-ttu-id="3e612-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e612-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3e612-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3e612-160">System.Int32</span></span>

## <span data-ttu-id="3e612-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e612-161">OUTPUTS</span></span>

### <span data-ttu-id="3e612-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e612-162">System.Boolean</span></span>

## <span data-ttu-id="3e612-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e612-163">NOTES</span></span>

## <span data-ttu-id="3e612-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e612-164">RELATED LINKS</span></span>

[<span data-ttu-id="3e612-165">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3e612-165">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


