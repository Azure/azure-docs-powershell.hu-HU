---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297749"
---
# <span data-ttu-id="c8529-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c8529-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="c8529-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8529-102">SYNOPSIS</span></span>
<span data-ttu-id="c8529-103">Módosította az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének bejegyzését.</span><span class="sxs-lookup"><span data-stu-id="c8529-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c8529-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8529-104">SYNTAX</span></span>

### <span data-ttu-id="c8529-105">SetByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8529-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8529-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="c8529-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8529-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8529-107">DESCRIPTION</span></span>
<span data-ttu-id="c8529-108">A **set-AzDataLakeStoreItemAclEntry** parancsmag az adattárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában szereplő bejegyzés (ACE) módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="c8529-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c8529-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c8529-109">EXAMPLES</span></span>

### <span data-ttu-id="c8529-110">Példa 1: ász engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c8529-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="c8529-111">Ez a parancs minden engedély birtokában módosítja az Patti-alapú ACE-t.</span><span class="sxs-lookup"><span data-stu-id="c8529-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="c8529-112">2. példa: az ACE rekurzív engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c8529-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="c8529-113">3. példa: az ACE rekurzív engedélyeinek módosítása az ACL-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="c8529-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="c8529-114">Ez a parancs rekurzívan módosította az Patti Fuller-t, hogy minden engedély a root-ra és annak összes alkönyvtárába és fájljára érvényes legyen.</span><span class="sxs-lookup"><span data-stu-id="c8529-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="c8529-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8529-115">PARAMETERS</span></span>

### <span data-ttu-id="c8529-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c8529-116">-Account</span></span>
<span data-ttu-id="c8529-117">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8529-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c8529-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="c8529-118">-AceType</span></span>
<span data-ttu-id="c8529-119">A módosítandó ász típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8529-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="c8529-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c8529-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8529-121">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="c8529-121">User</span></span> 
- <span data-ttu-id="c8529-122">Csoport</span><span class="sxs-lookup"><span data-stu-id="c8529-122">Group</span></span> 
- <span data-ttu-id="c8529-123">Maszk</span><span class="sxs-lookup"><span data-stu-id="c8529-123">Mask</span></span> 
- <span data-ttu-id="c8529-124">Más</span><span class="sxs-lookup"><span data-stu-id="c8529-124">Other</span></span>

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

### <span data-ttu-id="c8529-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="c8529-125">-Acl</span></span>
<span data-ttu-id="c8529-126">A módosítani kívánt bejegyzéseket tartalmazó ACL-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8529-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="c8529-127">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="c8529-127">-Concurrency</span></span>
<span data-ttu-id="c8529-128">A párhuzamosan feldolgozott fájlok/könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="c8529-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="c8529-129">Nem kötelező: a program megfelelő alapértelmezett beállítást ad meg.</span><span class="sxs-lookup"><span data-stu-id="c8529-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="c8529-130">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="c8529-130">-Default</span></span>
<span data-ttu-id="c8529-131">Jelzi, hogy ez a művelet módosította az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="c8529-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="c8529-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8529-132">-DefaultProfile</span></span>
<span data-ttu-id="c8529-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8529-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8529-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c8529-134">-Id</span></span>
<span data-ttu-id="c8529-135">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelybe az ACE-t módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="c8529-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="c8529-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8529-136">-PassThru</span></span>
<span data-ttu-id="c8529-137">Jelzi, hogy az eredményül kapott ACL-t vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="c8529-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="c8529-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c8529-138">-Path</span></span>
<span data-ttu-id="c8529-139">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre módosítani szeretne egy ÁSZT, kezdve a root (/) könyvtárral.</span><span class="sxs-lookup"><span data-stu-id="c8529-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c8529-140">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="c8529-140">-Permissions</span></span>
<span data-ttu-id="c8529-141">Megadja az ACE-nek szóló engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="c8529-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="c8529-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c8529-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8529-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="c8529-143">None</span></span>
- <span data-ttu-id="c8529-144">Végrehajtása</span><span class="sxs-lookup"><span data-stu-id="c8529-144">Execute</span></span>
- <span data-ttu-id="c8529-145">Írni</span><span class="sxs-lookup"><span data-stu-id="c8529-145">Write</span></span>
- <span data-ttu-id="c8529-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="c8529-146">WriteExecute</span></span>
- <span data-ttu-id="c8529-147">Olvasása</span><span class="sxs-lookup"><span data-stu-id="c8529-147">Read</span></span>
- <span data-ttu-id="c8529-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="c8529-148">ReadExecute</span></span>
- <span data-ttu-id="c8529-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c8529-149">ReadWrite</span></span>
- <span data-ttu-id="c8529-150">Minden</span><span class="sxs-lookup"><span data-stu-id="c8529-150">All</span></span>

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

### <span data-ttu-id="c8529-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="c8529-151">-Recurse</span></span>
<span data-ttu-id="c8529-152">Azt jelzi, hogy a rendszer rekurzív módon módosítsa a alárendelt alkönyvtárakra és fájlokra vonatkozó hozzáférés-vezérlési listákat.</span><span class="sxs-lookup"><span data-stu-id="c8529-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="c8529-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="c8529-153">-ShowProgress</span></span>
<span data-ttu-id="c8529-154">Ha a betelt, akkor a folyamat állapota látható.</span><span class="sxs-lookup"><span data-stu-id="c8529-154">If passed then progress status is showed.</span></span> <span data-ttu-id="c8529-155">Csak akkor érvényes, ha a rekurzív ACL módosítása befejeződött.</span><span class="sxs-lookup"><span data-stu-id="c8529-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="c8529-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8529-156">-Confirm</span></span>
<span data-ttu-id="c8529-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8529-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8529-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8529-158">-WhatIf</span></span>
<span data-ttu-id="c8529-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8529-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8529-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8529-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8529-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8529-161">CommonParameters</span></span>
<span data-ttu-id="c8529-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8529-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8529-163">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8529-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8529-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8529-164">INPUTS</span></span>

### <span data-ttu-id="c8529-165">System. String</span><span class="sxs-lookup"><span data-stu-id="c8529-165">System.String</span></span>

### <span data-ttu-id="c8529-166">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c8529-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c8529-167">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="c8529-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="c8529-168">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="c8529-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="c8529-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c8529-169">System.Guid</span></span>

### <span data-ttu-id="c8529-170">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + engedély</span><span class="sxs-lookup"><span data-stu-id="c8529-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="c8529-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8529-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c8529-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c8529-172">System.Int32</span></span>

## <span data-ttu-id="c8529-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8529-173">OUTPUTS</span></span>

### <span data-ttu-id="c8529-174">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="c8529-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="c8529-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8529-175">NOTES</span></span>

## <span data-ttu-id="c8529-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8529-176">RELATED LINKS</span></span>

[<span data-ttu-id="c8529-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c8529-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


