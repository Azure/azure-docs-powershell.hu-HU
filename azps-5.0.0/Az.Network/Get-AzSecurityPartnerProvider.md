---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195400"
---
# <span data-ttu-id="afd74-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="afd74-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="afd74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="afd74-102">SYNOPSIS</span></span>
<span data-ttu-id="afd74-103">Azure-SecurityPartnerProvider beszerzése</span><span class="sxs-lookup"><span data-stu-id="afd74-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="afd74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="afd74-104">SYNTAX</span></span>

### <span data-ttu-id="afd74-105">SecurityPartnerProviderNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="afd74-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afd74-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afd74-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afd74-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="afd74-107">DESCRIPTION</span></span>
<span data-ttu-id="afd74-108">A **Get-AzSecurityPartnerProvider** parancsmag Azure SecurityPartnerProvider kap</span><span class="sxs-lookup"><span data-stu-id="afd74-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="afd74-109">Példák</span><span class="sxs-lookup"><span data-stu-id="afd74-109">EXAMPLES</span></span>

### <span data-ttu-id="afd74-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="afd74-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="afd74-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="afd74-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="afd74-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="afd74-112">PARAMETERS</span></span>

### <span data-ttu-id="afd74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd74-113">-DefaultProfile</span></span>
<span data-ttu-id="afd74-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afd74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd74-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="afd74-115">-Name</span></span>
<span data-ttu-id="afd74-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="afd74-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd74-117">-ResourceGroupName</span></span>
<span data-ttu-id="afd74-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="afd74-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd74-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afd74-119">-ResourceId</span></span>
<span data-ttu-id="afd74-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="afd74-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd74-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd74-121">CommonParameters</span></span>
<span data-ttu-id="afd74-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="afd74-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd74-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="afd74-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd74-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="afd74-124">INPUTS</span></span>

### <span data-ttu-id="afd74-125">System. String</span><span class="sxs-lookup"><span data-stu-id="afd74-125">System.String</span></span>

## <span data-ttu-id="afd74-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afd74-126">OUTPUTS</span></span>

### <span data-ttu-id="afd74-127">Microsoft. Azure. commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="afd74-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="afd74-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="afd74-128">NOTES</span></span>

## <span data-ttu-id="afd74-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afd74-129">RELATED LINKS</span></span>