---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172877"
---
# <span data-ttu-id="5d448-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5d448-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5d448-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d448-102">SYNOPSIS</span></span>
<span data-ttu-id="5d448-103">A DNS-zóna csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="5d448-103">Updates DNS zone group</span></span>

## <span data-ttu-id="5d448-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d448-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d448-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d448-105">DESCRIPTION</span></span>
<span data-ttu-id="5d448-106">A **set-AzPrivateDnsZoneGroup** parancsmag frissíti a DNS Zone (DNS-zóna) csoportot.</span><span class="sxs-lookup"><span data-stu-id="5d448-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="5d448-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5d448-107">EXAMPLES</span></span>

### <span data-ttu-id="5d448-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5d448-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="5d448-109">A fenti példa frissíti a dnsgroup1 nevű DNS-zóna csoportot egy új dnsconfig, amely egy másik DNS-zónára hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5d448-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="5d448-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d448-110">PARAMETERS</span></span>

### <span data-ttu-id="5d448-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d448-111">-AsJob</span></span>
<span data-ttu-id="5d448-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5d448-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d448-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d448-113">-DefaultProfile</span></span>
<span data-ttu-id="5d448-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d448-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d448-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d448-115">-Name</span></span>
<span data-ttu-id="5d448-116">A privát DNS-zóna csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d448-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d448-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="5d448-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="5d448-118">A privát DNS-zóna csoport privát DNS-zóna-konfigurációjának gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="5d448-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d448-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="5d448-119">-PrivateEndpointName</span></span>
<span data-ttu-id="5d448-120">A privát végpont neve.</span><span class="sxs-lookup"><span data-stu-id="5d448-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="5d448-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d448-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d448-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d448-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d448-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d448-123">-Confirm</span></span>
<span data-ttu-id="5d448-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d448-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d448-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d448-125">-WhatIf</span></span>
<span data-ttu-id="5d448-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d448-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d448-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d448-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d448-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d448-128">CommonParameters</span></span>
<span data-ttu-id="5d448-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d448-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d448-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d448-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d448-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d448-131">INPUTS</span></span>

### <span data-ttu-id="5d448-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5d448-132">System.String</span></span>

### <span data-ttu-id="5d448-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 2.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5d448-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5d448-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d448-134">OUTPUTS</span></span>

### <span data-ttu-id="5d448-135">Microsoft. Azure. commands. Network. models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5d448-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5d448-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d448-136">NOTES</span></span>

## <span data-ttu-id="5d448-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d448-137">RELATED LINKS</span></span>
