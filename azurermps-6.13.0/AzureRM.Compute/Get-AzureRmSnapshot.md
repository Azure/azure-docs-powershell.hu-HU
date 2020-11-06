---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 14b1c1179e9fee15f398c4518e446cf47396e660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494132"
---
# <span data-ttu-id="9d356-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="9d356-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="9d356-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d356-102">SYNOPSIS</span></span>
<span data-ttu-id="9d356-103">A pillanatképek tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="9d356-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d356-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d356-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d356-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d356-105">DESCRIPTION</span></span>
<span data-ttu-id="9d356-106">A **Get-AzureRmSnapshot** parancsmag a pillanatképek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d356-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="9d356-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d356-107">EXAMPLES</span></span>

### <span data-ttu-id="9d356-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9d356-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="9d356-109">Ez a parancs megkapja az előfizetés összes pillanatképének tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="9d356-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="9d356-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="9d356-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="9d356-111">Ez a parancs a "ResourceGroupName1" nevű erőforráscsoport összes pillanatképének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d356-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="9d356-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="9d356-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="9d356-113">Ez a parancs a "ResourceGroupName1" nevű erőforráscsoport "SnapshotName1" nevű pillanatképének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d356-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="9d356-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d356-114">PARAMETERS</span></span>

### <span data-ttu-id="9d356-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d356-115">-DefaultProfile</span></span>
<span data-ttu-id="9d356-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d356-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d356-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d356-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d356-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d356-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d356-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9d356-119">-SnapshotName</span></span>
<span data-ttu-id="9d356-120">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d356-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d356-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d356-121">CommonParameters</span></span>
<span data-ttu-id="9d356-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d356-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d356-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d356-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d356-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d356-124">INPUTS</span></span>

### <span data-ttu-id="9d356-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9d356-125">System.String</span></span>

## <span data-ttu-id="9d356-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d356-126">OUTPUTS</span></span>

### <span data-ttu-id="9d356-127">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="9d356-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="9d356-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d356-128">NOTES</span></span>

## <span data-ttu-id="9d356-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d356-129">RELATED LINKS</span></span>
