---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160970"
---
# <span data-ttu-id="ed90d-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ed90d-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ed90d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed90d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed90d-103">Azure SecurityPartnerProvider-fiók lekérte</span><span class="sxs-lookup"><span data-stu-id="ed90d-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ed90d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed90d-104">SYNTAX</span></span>

### <span data-ttu-id="ed90d-105">SecurityPartnerProviderNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed90d-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed90d-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed90d-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed90d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed90d-107">DESCRIPTION</span></span>
<span data-ttu-id="ed90d-108">A **Get-AzSecurityPartnerProvider** parancsmag azure SecurityPartnerProvider-t kap</span><span class="sxs-lookup"><span data-stu-id="ed90d-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ed90d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed90d-109">EXAMPLES</span></span>

### <span data-ttu-id="ed90d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ed90d-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="ed90d-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="ed90d-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="ed90d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed90d-112">PARAMETERS</span></span>

### <span data-ttu-id="ed90d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed90d-113">-DefaultProfile</span></span>
<span data-ttu-id="ed90d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed90d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed90d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ed90d-115">-Name</span></span>
<span data-ttu-id="ed90d-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ed90d-116">The resource name.</span></span>

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

### <span data-ttu-id="ed90d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed90d-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed90d-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed90d-118">The resource group name.</span></span>

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

### <span data-ttu-id="ed90d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed90d-119">-ResourceId</span></span>
<span data-ttu-id="ed90d-120">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ed90d-120">The resource Id.</span></span>

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

### <span data-ttu-id="ed90d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed90d-121">CommonParameters</span></span>
<span data-ttu-id="ed90d-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed90d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed90d-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed90d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed90d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed90d-124">INPUTS</span></span>

### <span data-ttu-id="ed90d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ed90d-125">System.String</span></span>

## <span data-ttu-id="ed90d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed90d-126">OUTPUTS</span></span>

### <span data-ttu-id="ed90d-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ed90d-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ed90d-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed90d-128">NOTES</span></span>

## <span data-ttu-id="ed90d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed90d-129">RELATED LINKS</span></span>
