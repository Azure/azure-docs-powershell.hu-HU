---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 9ddd81b236303a15017bcd96da35774a16fae8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016181"
---
# <span data-ttu-id="d8494-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="d8494-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d8494-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8494-102">SYNOPSIS</span></span>
<span data-ttu-id="d8494-103">Frissítések DNS-zónacsoport</span><span class="sxs-lookup"><span data-stu-id="d8494-103">Updates DNS zone group</span></span>

## <span data-ttu-id="d8494-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8494-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8494-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8494-105">DESCRIPTION</span></span>
<span data-ttu-id="d8494-106">A **Set-AzPrivateDnsZoneGroup** parancsmag frissíti a DNS-zónacsoportot.</span><span class="sxs-lookup"><span data-stu-id="d8494-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="d8494-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8494-107">EXAMPLES</span></span>

### <span data-ttu-id="d8494-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d8494-108">Example 1</span></span>
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

<span data-ttu-id="d8494-109">A fenti példa frissíti a DNSGroup1 NEVŰ DNS-zónacsoportot egy új dnsconfig névvel, amely egy másik DNS-zónához kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="d8494-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="d8494-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8494-110">PARAMETERS</span></span>

### <span data-ttu-id="d8494-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8494-111">-AsJob</span></span>
<span data-ttu-id="d8494-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d8494-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8494-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8494-113">-DefaultProfile</span></span>
<span data-ttu-id="d8494-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8494-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8494-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d8494-115">-Name</span></span>
<span data-ttu-id="d8494-116">A privát DNS-zónacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8494-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="d8494-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="d8494-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="d8494-118">A privát DNS-zónacsoport privát DNS-zónakonfigurációinak gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="d8494-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="d8494-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="d8494-119">-PrivateEndpointName</span></span>
<span data-ttu-id="d8494-120">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="d8494-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="d8494-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8494-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8494-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8494-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8494-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8494-123">-Confirm</span></span>
<span data-ttu-id="d8494-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8494-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8494-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8494-125">-WhatIf</span></span>
<span data-ttu-id="d8494-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8494-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8494-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8494-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8494-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8494-128">CommonParameters</span></span>
<span data-ttu-id="d8494-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8494-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8494-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8494-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8494-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8494-131">INPUTS</span></span>

### <span data-ttu-id="d8494-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d8494-132">System.String</span></span>

### <span data-ttu-id="d8494-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d8494-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8494-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8494-134">OUTPUTS</span></span>

### <span data-ttu-id="d8494-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="d8494-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d8494-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8494-136">NOTES</span></span>

## <span data-ttu-id="d8494-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8494-137">RELATED LINKS</span></span>
