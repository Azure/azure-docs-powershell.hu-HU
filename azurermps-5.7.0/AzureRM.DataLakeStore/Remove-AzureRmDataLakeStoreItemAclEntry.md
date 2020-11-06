---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 41c1324c3762d0b6e04c0c532976c62c0a16067e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492290"
---
# <span data-ttu-id="8c312-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8c312-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="8c312-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c312-102">SYNOPSIS</span></span>
<span data-ttu-id="8c312-103">Az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének a bejegyzését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="8c312-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c312-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c312-104">SYNTAX</span></span>

### <span data-ttu-id="8c312-105">RemoveByACLObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c312-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c312-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="8c312-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c312-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c312-107">DESCRIPTION</span></span>
<span data-ttu-id="8c312-108">A **Remove-AzureRmDataLakeStoreItemAclEntry** parancsmag az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában található bejegyzés (ACE) eltávolítását távolítja el.</span><span class="sxs-lookup"><span data-stu-id="8c312-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8c312-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8c312-109">EXAMPLES</span></span>

### <span data-ttu-id="8c312-110">Példa 1: felhasználó bejegyzésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8c312-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="8c312-111">Ez a parancs eltávolítja a felhasználó ACE for Patti Fuller-t az ContosoADL-fiókból.</span><span class="sxs-lookup"><span data-stu-id="8c312-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="8c312-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c312-112">PARAMETERS</span></span>

### <span data-ttu-id="8c312-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="8c312-113">-Account</span></span>
<span data-ttu-id="8c312-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c312-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8c312-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="8c312-115">-AceType</span></span>
<span data-ttu-id="8c312-116">Az eltávolítandó ACE típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c312-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="8c312-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8c312-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c312-118">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="8c312-118">User</span></span>
- <span data-ttu-id="8c312-119">Csoport</span><span class="sxs-lookup"><span data-stu-id="8c312-119">Group</span></span>
- <span data-ttu-id="8c312-120">Maszk</span><span class="sxs-lookup"><span data-stu-id="8c312-120">Mask</span></span>
- <span data-ttu-id="8c312-121">Más</span><span class="sxs-lookup"><span data-stu-id="8c312-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: RemoveSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="8c312-122">-Acl</span></span>
<span data-ttu-id="8c312-123">Megadja az eltávolítandó bejegyzéseket tartalmazó ACL-objektumot.</span><span class="sxs-lookup"><span data-stu-id="8c312-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-124">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="8c312-124">-Default</span></span>
<span data-ttu-id="8c312-125">Azt jelzi, hogy ez a művelet eltávolítja az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="8c312-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c312-126">-DefaultProfile</span></span>
<span data-ttu-id="8c312-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c312-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c312-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8c312-128">-Id</span></span>
<span data-ttu-id="8c312-129">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelyből egy ÁSZT el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="8c312-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c312-130">-PassThru</span></span>
<span data-ttu-id="8c312-131">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8c312-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="8c312-132">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8c312-132">-Path</span></span>
<span data-ttu-id="8c312-133">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyből el szeretné távolítani az ÁSZT (/) a gyökérkönyvtártól kezdve.</span><span class="sxs-lookup"><span data-stu-id="8c312-133">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8c312-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c312-134">-Confirm</span></span>
<span data-ttu-id="8c312-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c312-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c312-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c312-136">-WhatIf</span></span>
<span data-ttu-id="8c312-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c312-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c312-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c312-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c312-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c312-139">CommonParameters</span></span>
<span data-ttu-id="8c312-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c312-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c312-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c312-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c312-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c312-142">INPUTS</span></span>

### <span data-ttu-id="8c312-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="8c312-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="8c312-144">Az "ACL" paraméter elfogadja a "DataLakeStoreItemAce []" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8c312-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="8c312-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c312-145">OUTPUTS</span></span>

### <span data-ttu-id="8c312-146">bool</span><span class="sxs-lookup"><span data-stu-id="8c312-146">bool</span></span>
<span data-ttu-id="8c312-147">Ha a PassThru meg van adva, akkor a sikeres befejezéshez az igaz értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8c312-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="8c312-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c312-148">NOTES</span></span>

## <span data-ttu-id="8c312-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c312-149">RELATED LINKS</span></span>

[<span data-ttu-id="8c312-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8c312-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


