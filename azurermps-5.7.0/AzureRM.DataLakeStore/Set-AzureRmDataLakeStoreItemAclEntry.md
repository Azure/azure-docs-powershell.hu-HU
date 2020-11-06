---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493133"
---
# <span data-ttu-id="28084-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="28084-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="28084-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28084-102">SYNOPSIS</span></span>
<span data-ttu-id="28084-103">Módosította az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének bejegyzését.</span><span class="sxs-lookup"><span data-stu-id="28084-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28084-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28084-104">SYNTAX</span></span>

### <span data-ttu-id="28084-105">SetByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28084-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28084-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="28084-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28084-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="28084-107">DESCRIPTION</span></span>
<span data-ttu-id="28084-108">A **set-AzureRmDataLakeStoreItemAclEntry** parancsmag az adattárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában szereplő bejegyzés (ACE) módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="28084-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="28084-109">Példák</span><span class="sxs-lookup"><span data-stu-id="28084-109">EXAMPLES</span></span>

### <span data-ttu-id="28084-110">Példa 1: ász engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="28084-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="28084-111">Ez a parancs minden engedély birtokában módosítja az Patti-alapú ACE-t.</span><span class="sxs-lookup"><span data-stu-id="28084-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="28084-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28084-112">PARAMETERS</span></span>

### <span data-ttu-id="28084-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="28084-113">-Account</span></span>
<span data-ttu-id="28084-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28084-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="28084-115">-AceType</span></span>
<span data-ttu-id="28084-116">A módosítandó ász típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28084-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="28084-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="28084-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28084-118">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="28084-118">User</span></span> 
- <span data-ttu-id="28084-119">Csoport</span><span class="sxs-lookup"><span data-stu-id="28084-119">Group</span></span> 
- <span data-ttu-id="28084-120">Maszk</span><span class="sxs-lookup"><span data-stu-id="28084-120">Mask</span></span> 
- <span data-ttu-id="28084-121">Más</span><span class="sxs-lookup"><span data-stu-id="28084-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="28084-122">-Acl</span></span>
<span data-ttu-id="28084-123">A módosítani kívánt bejegyzéseket tartalmazó ACL-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="28084-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-124">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="28084-124">-Default</span></span>
<span data-ttu-id="28084-125">Jelzi, hogy ez a művelet módosította az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="28084-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28084-126">-DefaultProfile</span></span>
<span data-ttu-id="28084-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28084-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28084-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="28084-128">-Id</span></span>
<span data-ttu-id="28084-129">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelybe az ACE-t módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="28084-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28084-130">-PassThru</span></span>
<span data-ttu-id="28084-131">Jelzi, hogy az eredményül kapott ACL-t vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="28084-131">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-132">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="28084-132">-Path</span></span>
<span data-ttu-id="28084-133">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre módosítani szeretne egy ÁSZT, kezdve a root (/) könyvtárral.</span><span class="sxs-lookup"><span data-stu-id="28084-133">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-134">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="28084-134">-Permissions</span></span>
<span data-ttu-id="28084-135">Megadja az ACE-nek szóló engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="28084-135">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="28084-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="28084-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28084-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="28084-137">None</span></span>
- <span data-ttu-id="28084-138">Végrehajtása</span><span class="sxs-lookup"><span data-stu-id="28084-138">Execute</span></span>
- <span data-ttu-id="28084-139">Írni</span><span class="sxs-lookup"><span data-stu-id="28084-139">Write</span></span>
- <span data-ttu-id="28084-140">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="28084-140">WriteExecute</span></span>
- <span data-ttu-id="28084-141">Olvasása</span><span class="sxs-lookup"><span data-stu-id="28084-141">Read</span></span>
- <span data-ttu-id="28084-142">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="28084-142">ReadExecute</span></span>
- <span data-ttu-id="28084-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="28084-143">ReadWrite</span></span>
- <span data-ttu-id="28084-144">Minden</span><span class="sxs-lookup"><span data-stu-id="28084-144">All</span></span>

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28084-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28084-145">-Confirm</span></span>
<span data-ttu-id="28084-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28084-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28084-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28084-147">-WhatIf</span></span>
<span data-ttu-id="28084-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28084-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28084-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28084-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28084-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28084-150">CommonParameters</span></span>
<span data-ttu-id="28084-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28084-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28084-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28084-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28084-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28084-153">INPUTS</span></span>

### <span data-ttu-id="28084-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="28084-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="28084-155">Az "ACL" paraméter elfogadja a "DataLakeStoreItemAce []" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="28084-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="28084-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28084-156">OUTPUTS</span></span>

### <span data-ttu-id="28084-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="28084-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="28084-158">Ha a PassThru meg van adva, az ACL-bejegyzések eredményül kapott listáját fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="28084-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="28084-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28084-159">NOTES</span></span>

## <span data-ttu-id="28084-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28084-160">RELATED LINKS</span></span>

[<span data-ttu-id="28084-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="28084-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


