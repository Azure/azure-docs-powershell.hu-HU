---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364040"
---
# <span data-ttu-id="b211d-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="b211d-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="b211d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b211d-102">SYNOPSIS</span></span>
<span data-ttu-id="b211d-103">Frissítések DNS-zónacsoport</span><span class="sxs-lookup"><span data-stu-id="b211d-103">Updates DNS zone group</span></span>

## <span data-ttu-id="b211d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b211d-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b211d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b211d-105">DESCRIPTION</span></span>
<span data-ttu-id="b211d-106">A **Set-AzPrivateDnsZoneGroup** parancsmag frissíti a DNS-zónacsoportot.</span><span class="sxs-lookup"><span data-stu-id="b211d-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="b211d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b211d-107">EXAMPLES</span></span>

### <span data-ttu-id="b211d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b211d-108">Example 1</span></span>
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

<span data-ttu-id="b211d-109">A fenti példa frissíti a DNSGroup1 NEVŰ DNS-zónacsoportot egy új dnsconfig névvel, amely egy másik DNS-zónához kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="b211d-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="b211d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b211d-110">PARAMETERS</span></span>

### <span data-ttu-id="b211d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b211d-111">-AsJob</span></span>
<span data-ttu-id="b211d-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b211d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b211d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b211d-113">-DefaultProfile</span></span>
<span data-ttu-id="b211d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b211d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b211d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b211d-115">-Name</span></span>
<span data-ttu-id="b211d-116">A privát DNS-zónacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b211d-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="b211d-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="b211d-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="b211d-118">A privát DNS-zónacsoport privát DNS-zónakonfigurációinak gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="b211d-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="b211d-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="b211d-119">-PrivateEndpointName</span></span>
<span data-ttu-id="b211d-120">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="b211d-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="b211d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b211d-121">-ResourceGroupName</span></span>
<span data-ttu-id="b211d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b211d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b211d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b211d-123">-Confirm</span></span>
<span data-ttu-id="b211d-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b211d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b211d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b211d-125">-WhatIf</span></span>
<span data-ttu-id="b211d-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b211d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b211d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b211d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b211d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b211d-128">CommonParameters</span></span>
<span data-ttu-id="b211d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b211d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b211d-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b211d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b211d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b211d-131">INPUTS</span></span>

### <span data-ttu-id="b211d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b211d-132">System.String</span></span>

### <span data-ttu-id="b211d-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b211d-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b211d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b211d-134">OUTPUTS</span></span>

### <span data-ttu-id="b211d-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="b211d-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="b211d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b211d-136">NOTES</span></span>

## <span data-ttu-id="b211d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b211d-137">RELATED LINKS</span></span>
