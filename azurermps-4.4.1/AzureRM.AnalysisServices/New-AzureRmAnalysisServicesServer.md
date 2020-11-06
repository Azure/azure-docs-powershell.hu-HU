---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492628"
---
# <span data-ttu-id="ca9ef-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ca9ef-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="ca9ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9ef-103">Új Analysis Services-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="ca9ef-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca9ef-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9ef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca9ef-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9ef-106">Az New-AzureRmAnalysisServicesServer parancsmag létrehoz egy új Analysis Services-kiszolgálót</span><span class="sxs-lookup"><span data-stu-id="ca9ef-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="ca9ef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca9ef-107">EXAMPLES</span></span>

### <span data-ttu-id="ca9ef-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca9ef-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="ca9ef-109">Létrehozza a TestServer nevű kiszolgálót az Azure region West-US és az erőforráscsoport testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="ca9ef-110">A kiszolgáló SKU-szintje S1 lesz.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="ca9ef-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca9ef-111">PARAMETERS</span></span>

### <span data-ttu-id="ca9ef-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="ca9ef-112">-Administrator</span></span>
<span data-ttu-id="ca9ef-113">A kiszolgálón rendszergazdaként beállítani kívánt felhasználók vagy csoportok vesszővel elválasztott listáját megadó karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="ca9ef-114">A felhasználóknak vagy csoportoknak megadni kell egy UPN-formátumot (például user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="ca9ef-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="ca9ef-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="ca9ef-116">A blob-tároló URI-ja az Analysis Services-kiszolgáló biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="ca9ef-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="ca9ef-117">-Location</span></span>
<span data-ttu-id="ca9ef-118">Az Azure-régió, ahol az Analysis Services-kiszolgáló van tárolva</span><span class="sxs-lookup"><span data-stu-id="ca9ef-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca9ef-119">-Name</span></span>
<span data-ttu-id="ca9ef-120">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="ca9ef-120">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca9ef-122">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="ca9ef-122">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="ca9ef-123">-Sku</span></span>
<span data-ttu-id="ca9ef-124">A kiszolgáló SKU-nak a neve.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="ca9ef-125">A támogatott értékek 0 ', ' 1 ', ' 2 ', ' 4 ', a standard réteghez "B1", "B2" az alapszinthez és a 'D 1 ' for Development Tier.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="ca9ef-126">-Tag</span></span>
<span data-ttu-id="ca9ef-127">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca9ef-128">-Confirm</span></span>
<span data-ttu-id="ca9ef-129">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="ca9ef-129">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9ef-130">-WhatIf</span></span>
<span data-ttu-id="ca9ef-131">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="ca9ef-131">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9ef-132">CommonParameters</span></span>
<span data-ttu-id="ca9ef-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca9ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9ef-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9ef-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9ef-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca9ef-135">INPUTS</span></span>

## <span data-ttu-id="ca9ef-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca9ef-136">OUTPUTS</span></span>

### <span data-ttu-id="ca9ef-137">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ca9ef-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="ca9ef-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca9ef-138">NOTES</span></span>
<span data-ttu-id="ca9ef-139">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="ca9ef-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="ca9ef-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca9ef-140">RELATED LINKS</span></span>

[<span data-ttu-id="ca9ef-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ca9ef-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="ca9ef-142">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ca9ef-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
