---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495888"
---
# <span data-ttu-id="4992d-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4992d-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="4992d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4992d-102">SYNOPSIS</span></span>
<span data-ttu-id="4992d-103">Új hálózati profil létrehozása.</span><span class="sxs-lookup"><span data-stu-id="4992d-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4992d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4992d-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4992d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4992d-105">DESCRIPTION</span></span>
<span data-ttu-id="4992d-106">A **New-AzureRmNetworkProfile** parancsmag új hálózati profil legfelső szintű erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4992d-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="4992d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4992d-107">EXAMPLES</span></span>

### <span data-ttu-id="4992d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4992d-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="4992d-109">Ezzel létrehoz egy új hálózati profil legfelső szintű erőforrást</span><span class="sxs-lookup"><span data-stu-id="4992d-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="4992d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4992d-110">PARAMETERS</span></span>

### <span data-ttu-id="4992d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4992d-111">-AsJob</span></span>
<span data-ttu-id="4992d-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4992d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4992d-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4992d-113">-ContainerNicConfig</span></span>
<span data-ttu-id="4992d-114">A hálózati profilba felvenni kívánt tároló hálózati adapter-konfigurációk.</span><span class="sxs-lookup"><span data-stu-id="4992d-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4992d-115">-DefaultProfile</span></span>
<span data-ttu-id="4992d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4992d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4992d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4992d-117">-Force</span></span>
<span data-ttu-id="4992d-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4992d-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4992d-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="4992d-119">-Location</span></span>
<span data-ttu-id="4992d-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="4992d-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4992d-121">-Name</span></span>
<span data-ttu-id="4992d-122">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="4992d-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4992d-123">-ResourceGroupName</span></span>
<span data-ttu-id="4992d-124">A hálózati profil erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4992d-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="4992d-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="4992d-125">-Tag</span></span>
<span data-ttu-id="4992d-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4992d-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4992d-127">-Confirm</span></span>
<span data-ttu-id="4992d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4992d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4992d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4992d-129">-WhatIf</span></span>
<span data-ttu-id="4992d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4992d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4992d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4992d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4992d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4992d-132">CommonParameters</span></span>
<span data-ttu-id="4992d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4992d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4992d-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4992d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4992d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4992d-135">INPUTS</span></span>

### <span data-ttu-id="4992d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4992d-136">System.String</span></span>

### <span data-ttu-id="4992d-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4992d-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4992d-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSContainerNetworkInterface, Microsoft. Azure. commands. Network, Version = 6.7.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4992d-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4992d-139">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSContainerNetworkInterfaceConfiguration, Microsoft. Azure. commands. Network, Version = 6.7.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4992d-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4992d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4992d-140">OUTPUTS</span></span>

### <span data-ttu-id="4992d-141">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4992d-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4992d-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4992d-142">NOTES</span></span>

## <span data-ttu-id="4992d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4992d-143">RELATED LINKS</span></span>
