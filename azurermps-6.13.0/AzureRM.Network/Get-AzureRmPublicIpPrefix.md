---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672472"
---
# <span data-ttu-id="4fd8d-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fd8d-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="4fd8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fd8d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd8d-103">Nyilvános IP-előtagot kap</span><span class="sxs-lookup"><span data-stu-id="4fd8d-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fd8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fd8d-104">SYNTAX</span></span>

### <span data-ttu-id="4fd8d-105">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="4fd8d-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fd8d-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fd8d-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fd8d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fd8d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd8d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fd8d-108">DESCRIPTION</span></span>
<span data-ttu-id="4fd8d-109">A **Get-AzureRmPublicIpPrefix** parancsmag egy vagy több nyilvános IP-előtagokat kap egy erőforráscsoport esetében.</span><span class="sxs-lookup"><span data-stu-id="4fd8d-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="4fd8d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4fd8d-110">EXAMPLES</span></span>

### <span data-ttu-id="4fd8d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4fd8d-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="4fd8d-112">Ez a parancs egy nyilvános IP-előtagot tartalmazó erőforrást kap, az erőforráscsoport $prefixName az erőforrás csoportban $rgName</span><span class="sxs-lookup"><span data-stu-id="4fd8d-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="4fd8d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fd8d-113">PARAMETERS</span></span>

### <span data-ttu-id="4fd8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd8d-114">-DefaultProfile</span></span>
<span data-ttu-id="4fd8d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fd8d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd8d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fd8d-116">-Name</span></span>
<span data-ttu-id="4fd8d-117">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4fd8d-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd8d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd8d-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fd8d-119">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4fd8d-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd8d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd8d-120">-ResourceId</span></span>
<span data-ttu-id="4fd8d-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4fd8d-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd8d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd8d-122">CommonParameters</span></span>
<span data-ttu-id="4fd8d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fd8d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4fd8d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd8d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd8d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fd8d-125">INPUTS</span></span>

### <span data-ttu-id="4fd8d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4fd8d-126">System.String</span></span>


## <span data-ttu-id="4fd8d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fd8d-127">OUTPUTS</span></span>

### <span data-ttu-id="4fd8d-128">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fd8d-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="4fd8d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fd8d-129">NOTES</span></span>

## <span data-ttu-id="4fd8d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fd8d-130">RELATED LINKS</span></span>
