---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466758"
---
# <span data-ttu-id="362f3-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="362f3-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="362f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="362f3-102">SYNOPSIS</span></span>
<span data-ttu-id="362f3-103">Létrehoz egy privát DNS-zónacsoportot a megadott privát végponton.</span><span class="sxs-lookup"><span data-stu-id="362f3-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="362f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="362f3-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="362f3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="362f3-105">DESCRIPTION</span></span>
<span data-ttu-id="362f3-106">A **New-AzPrivateDnsZoneGroup** parancsmag lehetővé teszi, hogy új privát DNS-zónacsoportot hozzon létre.</span><span class="sxs-lookup"><span data-stu-id="362f3-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="362f3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="362f3-107">EXAMPLES</span></span>

### <span data-ttu-id="362f3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="362f3-108">Example 1</span></span>
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

<span data-ttu-id="362f3-109">A privát végpont létrehozása után a fenti példa a DNS-zónacsoportot a magánjellegű végpont `test-pr-endpoint` alatt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="362f3-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="362f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="362f3-110">PARAMETERS</span></span>

### <span data-ttu-id="362f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="362f3-111">-AsJob</span></span>
<span data-ttu-id="362f3-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="362f3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="362f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362f3-113">-DefaultProfile</span></span>
<span data-ttu-id="362f3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="362f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="362f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="362f3-115">-Force</span></span>
<span data-ttu-id="362f3-116">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="362f3-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="362f3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="362f3-117">-Name</span></span>
<span data-ttu-id="362f3-118">A privát DNS-zónacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="362f3-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="362f3-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="362f3-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="362f3-120">A privát DNS-zónacsoport privát DNS-zónakonfigurációinak gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="362f3-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="362f3-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="362f3-121">-PrivateEndpointName</span></span>
<span data-ttu-id="362f3-122">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="362f3-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="362f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="362f3-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="362f3-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="362f3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="362f3-125">-Confirm</span></span>
<span data-ttu-id="362f3-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="362f3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="362f3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="362f3-127">-WhatIf</span></span>
<span data-ttu-id="362f3-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="362f3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="362f3-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="362f3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="362f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362f3-130">CommonParameters</span></span>
<span data-ttu-id="362f3-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362f3-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="362f3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362f3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="362f3-133">INPUTS</span></span>

### <span data-ttu-id="362f3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="362f3-134">System.String</span></span>

### <span data-ttu-id="362f3-135">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="362f3-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="362f3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="362f3-136">OUTPUTS</span></span>

### <span data-ttu-id="362f3-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="362f3-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="362f3-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="362f3-138">NOTES</span></span>

## <span data-ttu-id="362f3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="362f3-139">RELATED LINKS</span></span>
