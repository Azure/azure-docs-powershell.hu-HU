---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: f9428c2249cf69d366a6770d448e82618d98896f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919730"
---
# <span data-ttu-id="bdfab-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="bdfab-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="bdfab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdfab-102">SYNOPSIS</span></span>
<span data-ttu-id="bdfab-103">Privát DNS-zónacsoportot kap</span><span class="sxs-lookup"><span data-stu-id="bdfab-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="bdfab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bdfab-104">SYNTAX</span></span>

### <span data-ttu-id="bdfab-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdfab-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdfab-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="bdfab-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdfab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bdfab-107">DESCRIPTION</span></span>
<span data-ttu-id="bdfab-108">A **Get-AzPrivateDnsZoneGroup** parancsmag egy vagy több privát DNS-zónacsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="bdfab-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="bdfab-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bdfab-109">EXAMPLES</span></span>

### <span data-ttu-id="bdfab-110">1. példa: Privát DNS-zónacsoport lekérése</span><span class="sxs-lookup"><span data-stu-id="bdfab-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="bdfab-111">A fenti példa egy dnsgroup1 nevű privát DNS-zónacsoportot kap az rg erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="bdfab-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="bdfab-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdfab-112">PARAMETERS</span></span>

### <span data-ttu-id="bdfab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdfab-113">-DefaultProfile</span></span>
<span data-ttu-id="bdfab-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdfab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfab-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bdfab-115">-Name</span></span>
<span data-ttu-id="bdfab-116">A privát DNS-zónacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bdfab-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfab-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="bdfab-117">-PrivateEndpointName</span></span>
<span data-ttu-id="bdfab-118">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="bdfab-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdfab-119">-ResourceGroupName</span></span>
<span data-ttu-id="bdfab-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bdfab-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdfab-121">CommonParameters</span></span>
<span data-ttu-id="bdfab-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdfab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdfab-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdfab-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdfab-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdfab-124">INPUTS</span></span>

### <span data-ttu-id="bdfab-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bdfab-125">System.String</span></span>

## <span data-ttu-id="bdfab-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdfab-126">OUTPUTS</span></span>

### <span data-ttu-id="bdfab-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="bdfab-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="bdfab-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bdfab-128">NOTES</span></span>

## <span data-ttu-id="bdfab-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdfab-129">RELATED LINKS</span></span>
