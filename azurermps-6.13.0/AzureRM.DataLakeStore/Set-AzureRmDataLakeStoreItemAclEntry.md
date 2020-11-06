---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: acf0b53ba6ad03de117e9171ec64d30ee627a927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495155"
---
# <span data-ttu-id="e7502-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e7502-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="e7502-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7502-102">SYNOPSIS</span></span>
<span data-ttu-id="e7502-103">Módosította az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének bejegyzését.</span><span class="sxs-lookup"><span data-stu-id="e7502-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7502-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7502-104">SYNTAX</span></span>

### <span data-ttu-id="e7502-105">SetByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7502-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7502-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="e7502-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse]
 [-Concurrency <Int32>] [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7502-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7502-107">DESCRIPTION</span></span>
<span data-ttu-id="e7502-108">A **set-AzureRmDataLakeStoreItemAclEntry** parancsmag az adattárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában szereplő bejegyzés (ACE) módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="e7502-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e7502-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e7502-109">EXAMPLES</span></span>

### <span data-ttu-id="e7502-110">Példa 1: ász engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="e7502-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="e7502-111">Ez a parancs minden engedély birtokában módosítja az Patti-alapú ACE-t.</span><span class="sxs-lookup"><span data-stu-id="e7502-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="e7502-112">2. példa: az ACE rekurzív engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="e7502-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="e7502-113">3. példa: az ACE rekurzív engedélyeinek módosítása az ACL-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="e7502-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="e7502-114">Ez a parancs rekurzívan módosította az Patti Fuller-t, hogy minden engedély a root-ra és annak összes alkönyvtárába és fájljára érvényes legyen.</span><span class="sxs-lookup"><span data-stu-id="e7502-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="e7502-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7502-115">PARAMETERS</span></span>

### <span data-ttu-id="e7502-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="e7502-116">-Account</span></span>
<span data-ttu-id="e7502-117">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7502-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e7502-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="e7502-118">-AceType</span></span>
<span data-ttu-id="e7502-119">A módosítandó ász típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7502-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="e7502-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7502-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7502-121">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="e7502-121">User</span></span> 
- <span data-ttu-id="e7502-122">Csoport</span><span class="sxs-lookup"><span data-stu-id="e7502-122">Group</span></span> 
- <span data-ttu-id="e7502-123">Maszk</span><span class="sxs-lookup"><span data-stu-id="e7502-123">Mask</span></span> 
- <span data-ttu-id="e7502-124">Más</span><span class="sxs-lookup"><span data-stu-id="e7502-124">Other</span></span>

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

### <span data-ttu-id="e7502-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="e7502-125">-Acl</span></span>
<span data-ttu-id="e7502-126">A módosítani kívánt bejegyzéseket tartalmazó ACL-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7502-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="e7502-127">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="e7502-127">-Concurrency</span></span>
<span data-ttu-id="e7502-128">A párhuzamosan feldolgozott fájlok/könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="e7502-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="e7502-129">Nem kötelező: a program megfelelő alapértelmezett beállítást ad meg.</span><span class="sxs-lookup"><span data-stu-id="e7502-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="e7502-130">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="e7502-130">-Default</span></span>
<span data-ttu-id="e7502-131">Jelzi, hogy ez a művelet módosította az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="e7502-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="e7502-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7502-132">-DefaultProfile</span></span>
<span data-ttu-id="e7502-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7502-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7502-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e7502-134">-Id</span></span>
<span data-ttu-id="e7502-135">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelybe az ACE-t módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="e7502-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="e7502-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7502-136">-PassThru</span></span>
<span data-ttu-id="e7502-137">Jelzi, hogy az eredményül kapott ACL-t vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="e7502-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="e7502-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e7502-138">-Path</span></span>
<span data-ttu-id="e7502-139">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre módosítani szeretne egy ÁSZT, kezdve a root (/) könyvtárral.</span><span class="sxs-lookup"><span data-stu-id="e7502-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e7502-140">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="e7502-140">-Permissions</span></span>
<span data-ttu-id="e7502-141">Megadja az ACE-nek szóló engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="e7502-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="e7502-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7502-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7502-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7502-143">None</span></span>
- <span data-ttu-id="e7502-144">Végrehajtása</span><span class="sxs-lookup"><span data-stu-id="e7502-144">Execute</span></span>
- <span data-ttu-id="e7502-145">Írni</span><span class="sxs-lookup"><span data-stu-id="e7502-145">Write</span></span>
- <span data-ttu-id="e7502-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="e7502-146">WriteExecute</span></span>
- <span data-ttu-id="e7502-147">Olvasása</span><span class="sxs-lookup"><span data-stu-id="e7502-147">Read</span></span>
- <span data-ttu-id="e7502-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="e7502-148">ReadExecute</span></span>
- <span data-ttu-id="e7502-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e7502-149">ReadWrite</span></span>
- <span data-ttu-id="e7502-150">Minden</span><span class="sxs-lookup"><span data-stu-id="e7502-150">All</span></span>

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

### <span data-ttu-id="e7502-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e7502-151">-Recurse</span></span>
<span data-ttu-id="e7502-152">Azt jelzi, hogy a rendszer rekurzív módon módosítsa a alárendelt alkönyvtárakra és fájlokra vonatkozó hozzáférés-vezérlési listákat.</span><span class="sxs-lookup"><span data-stu-id="e7502-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="e7502-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="e7502-153">-ShowProgress</span></span>
<span data-ttu-id="e7502-154">Ha a betelt, akkor a folyamat állapota látható.</span><span class="sxs-lookup"><span data-stu-id="e7502-154">If passed then progress status is showed.</span></span> <span data-ttu-id="e7502-155">Csak akkor érvényes, ha a rekurzív ACL módosítása befejeződött.</span><span class="sxs-lookup"><span data-stu-id="e7502-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="e7502-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7502-156">-Confirm</span></span>
<span data-ttu-id="e7502-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7502-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7502-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7502-158">-WhatIf</span></span>
<span data-ttu-id="e7502-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7502-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7502-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7502-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7502-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7502-161">CommonParameters</span></span>
<span data-ttu-id="e7502-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7502-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7502-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7502-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7502-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7502-164">INPUTS</span></span>

### <span data-ttu-id="e7502-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e7502-165">System.String</span></span>

### <span data-ttu-id="e7502-166">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e7502-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e7502-167">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="e7502-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="e7502-168">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="e7502-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="e7502-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e7502-169">System.Guid</span></span>

### <span data-ttu-id="e7502-170">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + engedély</span><span class="sxs-lookup"><span data-stu-id="e7502-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="e7502-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7502-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e7502-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e7502-172">System.Int32</span></span>

## <span data-ttu-id="e7502-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7502-173">OUTPUTS</span></span>

### <span data-ttu-id="e7502-174">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="e7502-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="e7502-175">Ha a PassThru meg van adva, az ACL-bejegyzések eredményül kapott listáját fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="e7502-175">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="e7502-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7502-176">NOTES</span></span>

## <span data-ttu-id="e7502-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7502-177">RELATED LINKS</span></span>

[<span data-ttu-id="e7502-178">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e7502-178">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


