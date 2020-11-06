---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504179"
---
# <span data-ttu-id="f489a-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f489a-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="f489a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f489a-102">SYNOPSIS</span></span>
<span data-ttu-id="f489a-103">Módosította az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének bejegyzését.</span><span class="sxs-lookup"><span data-stu-id="f489a-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f489a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f489a-104">SYNTAX</span></span>

### <span data-ttu-id="f489a-105">ACL-bejegyzések beállítása az ACL-objektummal (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f489a-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f489a-106">Adott ACE beállítása</span><span class="sxs-lookup"><span data-stu-id="f489a-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f489a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f489a-107">DESCRIPTION</span></span>
<span data-ttu-id="f489a-108">A **set-AzureRmDataLakeStoreItemAclEntry** parancsmag az adattárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában szereplő bejegyzés (ACE) módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="f489a-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f489a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f489a-109">EXAMPLES</span></span>

### <span data-ttu-id="f489a-110">Példa 1: ász engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="f489a-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="f489a-111">Ez a parancs minden engedély birtokában módosítja az Patti-alapú ACE-t.</span><span class="sxs-lookup"><span data-stu-id="f489a-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="f489a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f489a-112">PARAMETERS</span></span>

### <span data-ttu-id="f489a-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="f489a-113">-Account</span></span>
<span data-ttu-id="f489a-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f489a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f489a-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="f489a-115">-AceType</span></span>
<span data-ttu-id="f489a-116">A módosítandó ász típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f489a-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="f489a-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f489a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f489a-118">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="f489a-118">User</span></span> 
- <span data-ttu-id="f489a-119">Csoport</span><span class="sxs-lookup"><span data-stu-id="f489a-119">Group</span></span> 
- <span data-ttu-id="f489a-120">Maszk</span><span class="sxs-lookup"><span data-stu-id="f489a-120">Mask</span></span> 
- <span data-ttu-id="f489a-121">Más</span><span class="sxs-lookup"><span data-stu-id="f489a-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f489a-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="f489a-122">-Acl</span></span>
<span data-ttu-id="f489a-123">A módosítani kívánt bejegyzéseket tartalmazó ACL-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f489a-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f489a-124">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="f489a-124">-Default</span></span>
<span data-ttu-id="f489a-125">Jelzi, hogy ez a művelet módosította az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="f489a-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f489a-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f489a-126">-Id</span></span>
<span data-ttu-id="f489a-127">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelybe az ACE-t módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="f489a-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f489a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f489a-128">-PassThru</span></span>
<span data-ttu-id="f489a-129">Jelzi, hogy az eredményül kapott ACL-t vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="f489a-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="f489a-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="f489a-130">-Path</span></span>
<span data-ttu-id="f489a-131">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre módosítani szeretne egy ÁSZT, kezdve a root (/) könyvtárral.</span><span class="sxs-lookup"><span data-stu-id="f489a-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f489a-132">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="f489a-132">-Permissions</span></span>
<span data-ttu-id="f489a-133">Megadja az ACE-nek szóló engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="f489a-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="f489a-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f489a-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f489a-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="f489a-135">None</span></span>
- <span data-ttu-id="f489a-136">Végrehajtása</span><span class="sxs-lookup"><span data-stu-id="f489a-136">Execute</span></span>
- <span data-ttu-id="f489a-137">Írni</span><span class="sxs-lookup"><span data-stu-id="f489a-137">Write</span></span>
- <span data-ttu-id="f489a-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="f489a-138">WriteExecute</span></span>
- <span data-ttu-id="f489a-139">Olvasása</span><span class="sxs-lookup"><span data-stu-id="f489a-139">Read</span></span>
- <span data-ttu-id="f489a-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="f489a-140">ReadExecute</span></span>
- <span data-ttu-id="f489a-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f489a-141">ReadWrite</span></span>
- <span data-ttu-id="f489a-142">Minden</span><span class="sxs-lookup"><span data-stu-id="f489a-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f489a-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f489a-143">-Confirm</span></span>
<span data-ttu-id="f489a-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f489a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f489a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f489a-145">-WhatIf</span></span>
<span data-ttu-id="f489a-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f489a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f489a-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f489a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f489a-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f489a-148">-DefaultProfile</span></span>
<span data-ttu-id="f489a-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f489a-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f489a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f489a-150">CommonParameters</span></span>
<span data-ttu-id="f489a-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f489a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f489a-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f489a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f489a-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f489a-153">INPUTS</span></span>

### <span data-ttu-id="f489a-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="f489a-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="f489a-155">Az "ACL" paraméter elfogadja a "DataLakeStoreItemAce []" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f489a-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="f489a-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f489a-156">OUTPUTS</span></span>

### <span data-ttu-id="f489a-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="f489a-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="f489a-158">Ha a PassThru meg van adva, az ACL-bejegyzések eredményül kapott listáját fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="f489a-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="f489a-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f489a-159">NOTES</span></span>

## <span data-ttu-id="f489a-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f489a-160">RELATED LINKS</span></span>

[<span data-ttu-id="f489a-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f489a-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


