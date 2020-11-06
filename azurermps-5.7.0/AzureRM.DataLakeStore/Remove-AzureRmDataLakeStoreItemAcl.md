---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 23eb57a6c12c3ce5ba8334b7309b5c282624620a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492287"
---
# <span data-ttu-id="6705d-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6705d-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="6705d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6705d-102">SYNOPSIS</span></span>
<span data-ttu-id="6705d-103">Törli az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="6705d-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6705d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6705d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6705d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6705d-105">DESCRIPTION</span></span>
<span data-ttu-id="6705d-106">A **Remove-AzureRmDataLakeStoreItemAcl** parancsmag törli az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="6705d-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6705d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6705d-107">EXAMPLES</span></span>

### <span data-ttu-id="6705d-108">1. példa: az ACL eltávolítása mappából</span><span class="sxs-lookup"><span data-stu-id="6705d-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="6705d-109">Ez a parancs eltávolítja az ContosoADL-fiók gyökérkönyvtárának hozzáférés-vezérlési mappáját.</span><span class="sxs-lookup"><span data-stu-id="6705d-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="6705d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6705d-110">PARAMETERS</span></span>

### <span data-ttu-id="6705d-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="6705d-111">-Account</span></span>
<span data-ttu-id="6705d-112">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6705d-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="6705d-113">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="6705d-113">-Default</span></span>
<span data-ttu-id="6705d-114">Azt jelzi, hogy a parancsmag eltávolítja egy fájl vagy mappa alapértelmezett hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="6705d-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6705d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6705d-115">-DefaultProfile</span></span>
<span data-ttu-id="6705d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6705d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6705d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6705d-117">-Force</span></span>
<span data-ttu-id="6705d-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6705d-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6705d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6705d-119">-PassThru</span></span>
<span data-ttu-id="6705d-120">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6705d-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6705d-121">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="6705d-121">-Path</span></span>
<span data-ttu-id="6705d-122">Az elem az adattó-tároló elérési útját adja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="6705d-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6705d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6705d-123">-Confirm</span></span>
<span data-ttu-id="6705d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6705d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6705d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6705d-125">-WhatIf</span></span>
<span data-ttu-id="6705d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6705d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6705d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6705d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6705d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6705d-128">CommonParameters</span></span>
<span data-ttu-id="6705d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6705d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6705d-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6705d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6705d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6705d-131">INPUTS</span></span>

### <span data-ttu-id="6705d-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="6705d-132">None</span></span>
<span data-ttu-id="6705d-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6705d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6705d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6705d-134">OUTPUTS</span></span>

### <span data-ttu-id="6705d-135">bool</span><span class="sxs-lookup"><span data-stu-id="6705d-135">bool</span></span>
<span data-ttu-id="6705d-136">Ha a PassThru meg van adva, akkor a sikeres befejezéshez az igaz értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6705d-136">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="6705d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6705d-137">NOTES</span></span>
* <span data-ttu-id="6705d-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="6705d-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="6705d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6705d-139">RELATED LINKS</span></span>

[<span data-ttu-id="6705d-140">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6705d-140">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="6705d-141">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6705d-141">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="6705d-142">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6705d-142">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


