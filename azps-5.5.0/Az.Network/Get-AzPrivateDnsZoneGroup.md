---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160986"
---
# <span data-ttu-id="99882-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="99882-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="99882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99882-102">SYNOPSIS</span></span>
<span data-ttu-id="99882-103">Privát DNS-zónacsoportot kap</span><span class="sxs-lookup"><span data-stu-id="99882-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="99882-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99882-104">SYNTAX</span></span>

### <span data-ttu-id="99882-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99882-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99882-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="99882-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99882-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99882-107">DESCRIPTION</span></span>
<span data-ttu-id="99882-108">A **Get-AzPrivateDnsZoneGroup** parancsmag egy vagy több privát DNS-zónacsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="99882-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="99882-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99882-109">EXAMPLES</span></span>

### <span data-ttu-id="99882-110">1. példa: Privát DNS-zónacsoport lekérése</span><span class="sxs-lookup"><span data-stu-id="99882-110">Example 1: Retrieve private DNS zone group</span></span>
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

<span data-ttu-id="99882-111">A fenti példa egy dnsgroup1 nevű privát DNS-zónacsoportot kap az rg erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="99882-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="99882-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99882-112">PARAMETERS</span></span>

### <span data-ttu-id="99882-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99882-113">-DefaultProfile</span></span>
<span data-ttu-id="99882-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99882-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99882-115">-Name</span><span class="sxs-lookup"><span data-stu-id="99882-115">-Name</span></span>
<span data-ttu-id="99882-116">A privát DNS-zónacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="99882-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="99882-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="99882-117">-PrivateEndpointName</span></span>
<span data-ttu-id="99882-118">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="99882-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="99882-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99882-119">-ResourceGroupName</span></span>
<span data-ttu-id="99882-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="99882-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="99882-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99882-121">CommonParameters</span></span>
<span data-ttu-id="99882-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99882-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99882-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99882-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99882-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99882-124">INPUTS</span></span>

### <span data-ttu-id="99882-125">System.String</span><span class="sxs-lookup"><span data-stu-id="99882-125">System.String</span></span>

## <span data-ttu-id="99882-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99882-126">OUTPUTS</span></span>

### <span data-ttu-id="99882-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="99882-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="99882-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99882-128">NOTES</span></span>

## <span data-ttu-id="99882-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99882-129">RELATED LINKS</span></span>
