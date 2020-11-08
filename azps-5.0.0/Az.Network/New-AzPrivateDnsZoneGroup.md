---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194541"
---
# <span data-ttu-id="e6ac9-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="e6ac9-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="e6ac9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ac9-103">Egy privát DNS-zóna csoportot hoz létre a megadott privát végpontban.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="e6ac9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6ac9-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ac9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ac9-106">A **New-AzPrivateDnsZoneGroup** parancsmag lehetővé teszi új privát DNS-zóna csoport létrehozását.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="e6ac9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="e6ac9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6ac9-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
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

<span data-ttu-id="e6ac9-109">Miután `test-pr-endpoint` létrehozta a privát végpontot, a fenti példa létrehozza a DNS Zone (DNS-zóna) csoportot az adott privát végpont alatt.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="e6ac9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6ac9-110">PARAMETERS</span></span>

### <span data-ttu-id="e6ac9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6ac9-111">-AsJob</span></span>
<span data-ttu-id="e6ac9-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6ac9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6ac9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ac9-113">-DefaultProfile</span></span>
<span data-ttu-id="e6ac9-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ac9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e6ac9-115">-Force</span></span>
<span data-ttu-id="e6ac9-116">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e6ac9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6ac9-117">-Name</span></span>
<span data-ttu-id="e6ac9-118">A privát DNS-zóna csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="e6ac9-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="e6ac9-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="e6ac9-120">A privát DNS-zóna csoport privát DNS-zóna-konfigurációjának gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="e6ac9-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="e6ac9-121">-PrivateEndpointName</span></span>
<span data-ttu-id="e6ac9-122">A privát végpont neve.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="e6ac9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ac9-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6ac9-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6ac9-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6ac9-125">-Confirm</span></span>
<span data-ttu-id="e6ac9-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ac9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ac9-127">-WhatIf</span></span>
<span data-ttu-id="e6ac9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ac9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ac9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ac9-130">CommonParameters</span></span>
<span data-ttu-id="e6ac9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6ac9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ac9-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6ac9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ac9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ac9-133">INPUTS</span></span>

### <span data-ttu-id="e6ac9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e6ac9-134">System.String</span></span>

### <span data-ttu-id="e6ac9-135">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 2.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e6ac9-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6ac9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ac9-136">OUTPUTS</span></span>

### <span data-ttu-id="e6ac9-137">Microsoft. Azure. commands. Network. models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="e6ac9-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="e6ac9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6ac9-138">NOTES</span></span>

## <span data-ttu-id="e6ac9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6ac9-139">RELATED LINKS</span></span>
