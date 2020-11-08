---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: e463e6a1d25db24553b62c8d2fea1051eb231840
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012062"
---
# <span data-ttu-id="65815-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65815-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="65815-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65815-102">SYNOPSIS</span></span>
<span data-ttu-id="65815-103">Új hálózati profil létrehozása.</span><span class="sxs-lookup"><span data-stu-id="65815-103">Creates a new network profile.</span></span>

## <span data-ttu-id="65815-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65815-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65815-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65815-105">DESCRIPTION</span></span>
<span data-ttu-id="65815-106">A **New-AzNetworkProfile** parancsmag új hálózati profil legfelső szintű erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="65815-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="65815-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65815-107">EXAMPLES</span></span>

### <span data-ttu-id="65815-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65815-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="65815-109">Ezzel létrehoz egy új hálózati profil legfelső szintű erőforrást</span><span class="sxs-lookup"><span data-stu-id="65815-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="65815-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65815-110">PARAMETERS</span></span>

### <span data-ttu-id="65815-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65815-111">-AsJob</span></span>
<span data-ttu-id="65815-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65815-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65815-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="65815-113">-ContainerNicConfig</span></span>
<span data-ttu-id="65815-114">A hálózati profilba felvenni kívánt tároló hálózati adapter-konfigurációk.</span><span class="sxs-lookup"><span data-stu-id="65815-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="65815-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65815-115">-DefaultProfile</span></span>
<span data-ttu-id="65815-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65815-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65815-117">-Force</span><span class="sxs-lookup"><span data-stu-id="65815-117">-Force</span></span>
<span data-ttu-id="65815-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65815-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="65815-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="65815-119">-Location</span></span>
<span data-ttu-id="65815-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="65815-120">The location.</span></span>

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

### <span data-ttu-id="65815-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65815-121">-Name</span></span>
<span data-ttu-id="65815-122">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="65815-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="65815-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65815-123">-ResourceGroupName</span></span>
<span data-ttu-id="65815-124">A hálózati profil erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="65815-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="65815-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="65815-125">-Tag</span></span>
<span data-ttu-id="65815-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="65815-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="65815-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65815-127">-Confirm</span></span>
<span data-ttu-id="65815-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65815-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65815-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65815-129">-WhatIf</span></span>
<span data-ttu-id="65815-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65815-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65815-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65815-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65815-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65815-132">CommonParameters</span></span>
<span data-ttu-id="65815-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65815-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65815-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65815-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65815-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65815-135">INPUTS</span></span>

### <span data-ttu-id="65815-136">System. String</span><span class="sxs-lookup"><span data-stu-id="65815-136">System.String</span></span>

### <span data-ttu-id="65815-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65815-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="65815-138">Microsoft. Azure. commands. Network. models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="65815-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="65815-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65815-139">OUTPUTS</span></span>

### <span data-ttu-id="65815-140">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65815-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="65815-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65815-141">NOTES</span></span>

## <span data-ttu-id="65815-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65815-142">RELATED LINKS</span></span>

[<span data-ttu-id="65815-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65815-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="65815-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65815-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="65815-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65815-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
