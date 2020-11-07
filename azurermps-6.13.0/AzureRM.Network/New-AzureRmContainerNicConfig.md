---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680640"
---
# <span data-ttu-id="22852-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="22852-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="22852-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22852-102">SYNOPSIS</span></span>
<span data-ttu-id="22852-103">Új tároló hálózati csatoló konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="22852-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22852-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22852-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22852-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22852-105">DESCRIPTION</span></span>
<span data-ttu-id="22852-106">A **New-AzureRmNetworkProfileContainerNicConfig** parancsmag létrehoz egy új tároló hálózati adapter-konfiguráció objektumát.</span><span class="sxs-lookup"><span data-stu-id="22852-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="22852-107">Ez az objektum a hálózat hálózati profiljára hivatkozó hálózati interfacs jellemzőit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="22852-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="22852-108">Példák</span><span class="sxs-lookup"><span data-stu-id="22852-108">EXAMPLES</span></span>

### <span data-ttu-id="22852-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="22852-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="22852-110">Az első parancs létrehoz egy üres tároló hálózati illesztőfelület-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="22852-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="22852-111">A második létrehoz egy új hálózati profilt, amely a korábban létrehozott tároló hálózati felületének konfigurációját az New-NetworkProfile parancsmag argumentumaként adja meg.</span><span class="sxs-lookup"><span data-stu-id="22852-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="22852-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22852-112">PARAMETERS</span></span>

### <span data-ttu-id="22852-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22852-113">-DefaultProfile</span></span>
<span data-ttu-id="22852-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22852-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22852-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="22852-115">-IpConfiguration</span></span>
<span data-ttu-id="22852-116">{{Fill IpConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="22852-116">{{Fill IpConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22852-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22852-117">-Name</span></span>
<span data-ttu-id="22852-118">A tároló hálózati felületének konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="22852-118">Name of the container network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22852-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22852-119">-Confirm</span></span>
<span data-ttu-id="22852-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22852-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22852-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22852-121">-WhatIf</span></span>
<span data-ttu-id="22852-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22852-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22852-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22852-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22852-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22852-124">CommonParameters</span></span>
<span data-ttu-id="22852-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22852-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22852-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22852-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22852-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22852-127">INPUTS</span></span>

### <span data-ttu-id="22852-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSIPConfigurationProfile, Microsoft. Azure. commands. Network, Version = 6.7.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22852-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="22852-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22852-129">OUTPUTS</span></span>

### <span data-ttu-id="22852-130">Microsoft. Azure. commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="22852-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="22852-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22852-131">NOTES</span></span>

## <span data-ttu-id="22852-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22852-132">RELATED LINKS</span></span>
