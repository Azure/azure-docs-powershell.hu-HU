---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 99498979df259723a192bd0e2fd74ef436ae0ee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919634"
---
# <span data-ttu-id="90612-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="90612-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="90612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90612-102">SYNOPSIS</span></span>
<span data-ttu-id="90612-103">Azure SecurityPartnerProvider-fiók lekérte</span><span class="sxs-lookup"><span data-stu-id="90612-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="90612-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90612-104">SYNTAX</span></span>

### <span data-ttu-id="90612-105">SecurityPartnerProviderNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90612-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90612-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90612-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90612-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90612-107">DESCRIPTION</span></span>
<span data-ttu-id="90612-108">A **Get-AzSecurityPartnerProvider** parancsmag azure SecurityPartnerProvider-t kap</span><span class="sxs-lookup"><span data-stu-id="90612-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="90612-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90612-109">EXAMPLES</span></span>

### <span data-ttu-id="90612-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="90612-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="90612-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="90612-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="90612-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90612-112">PARAMETERS</span></span>

### <span data-ttu-id="90612-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90612-113">-DefaultProfile</span></span>
<span data-ttu-id="90612-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90612-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90612-115">-Name</span><span class="sxs-lookup"><span data-stu-id="90612-115">-Name</span></span>
<span data-ttu-id="90612-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="90612-116">The resource name.</span></span>

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

### <span data-ttu-id="90612-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90612-117">-ResourceGroupName</span></span>
<span data-ttu-id="90612-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="90612-118">The resource group name.</span></span>

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

### <span data-ttu-id="90612-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90612-119">-ResourceId</span></span>
<span data-ttu-id="90612-120">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="90612-120">The resource Id.</span></span>

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

### <span data-ttu-id="90612-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90612-121">CommonParameters</span></span>
<span data-ttu-id="90612-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90612-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90612-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90612-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90612-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90612-124">INPUTS</span></span>

### <span data-ttu-id="90612-125">System.String</span><span class="sxs-lookup"><span data-stu-id="90612-125">System.String</span></span>

## <span data-ttu-id="90612-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90612-126">OUTPUTS</span></span>

### <span data-ttu-id="90612-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="90612-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="90612-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90612-128">NOTES</span></span>

## <span data-ttu-id="90612-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90612-129">RELATED LINKS</span></span>
