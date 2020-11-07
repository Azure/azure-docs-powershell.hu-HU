---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: eb88be102f390d9e94ba938eeb6d116af6a79fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837262"
---
# <span data-ttu-id="a5eff-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="a5eff-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="a5eff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5eff-102">SYNOPSIS</span></span>
<span data-ttu-id="a5eff-103">Információt kap a VPN-ügyfél csomagról.</span><span class="sxs-lookup"><span data-stu-id="a5eff-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="a5eff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5eff-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5eff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5eff-105">DESCRIPTION</span></span>
<span data-ttu-id="a5eff-106">A **Get-AzVpnClientPackage** parancsmag információt kap a virtuális hálózati átjáróból elérhető VPN-ügyfél-csomagokról.</span><span class="sxs-lookup"><span data-stu-id="a5eff-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="a5eff-107">Az ügyfél csomagjai olyan konfigurációs adatokat tartalmaznak, amelyek lehetővé teszik, hogy egy ügyfélszámítógép virtuális MAGÁNHÁLÓZATI kapcsolatot hozzon létre egy Azure virtuális hálózattal; a VPN-kapcsolat létrehozásához az ügyfélgépeknek telepítve kell lenniük a megfelelő konfigurációs csomagnak.</span><span class="sxs-lookup"><span data-stu-id="a5eff-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="a5eff-108">Az ügyfélszámítógép Windows-verziójának (például a Windows 7 vagy a Windows 10) és az ügyfélszámítógép processzor-architektúrájának (AMD64 vagy x86) alapján is elérhetők a különféle konfigurációs csomagok.</span><span class="sxs-lookup"><span data-stu-id="a5eff-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="a5eff-109">A **Get-AzVpnClientPackage** futtatásakor meg kell adnia az architektúra típusát.</span><span class="sxs-lookup"><span data-stu-id="a5eff-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="a5eff-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a5eff-110">EXAMPLES</span></span>

### <span data-ttu-id="a5eff-111">1. példa: adatok beszerzése a processzor-architektúra VPN-csomagról</span><span class="sxs-lookup"><span data-stu-id="a5eff-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="a5eff-112">Ez a parancs információt kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróban tárolt AMD64 VPN-csomagokról.</span><span class="sxs-lookup"><span data-stu-id="a5eff-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="a5eff-113">Ha információkat szeretne kapni az x86-os ügyfél-csomagokról, állítsa az *ProcessorArchitecture* paraméter értékét x86 értékre.</span><span class="sxs-lookup"><span data-stu-id="a5eff-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="a5eff-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5eff-114">PARAMETERS</span></span>

### <span data-ttu-id="a5eff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5eff-115">-DefaultProfile</span></span>
<span data-ttu-id="a5eff-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5eff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5eff-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="a5eff-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="a5eff-118">Annak a CPU-architektúrának a típusát adja meg, amelyre az ügyfél-csomag van tervezve.</span><span class="sxs-lookup"><span data-stu-id="a5eff-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="a5eff-119">Az érvényes értékek az Amd64 és az x86.</span><span class="sxs-lookup"><span data-stu-id="a5eff-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5eff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5eff-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5eff-121">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a5eff-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="a5eff-122">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="a5eff-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5eff-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a5eff-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a5eff-124">Annak a virtuális hálózati átjárónak a neve, amelybe az ügyfél-csomag adatai vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="a5eff-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5eff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5eff-125">CommonParameters</span></span>
<span data-ttu-id="a5eff-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5eff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5eff-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a5eff-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5eff-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5eff-128">INPUTS</span></span>

### <span data-ttu-id="a5eff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a5eff-129">System.String</span></span>

## <span data-ttu-id="a5eff-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5eff-130">OUTPUTS</span></span>

### <span data-ttu-id="a5eff-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a5eff-131">System.String</span></span>

## <span data-ttu-id="a5eff-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5eff-132">NOTES</span></span>

## <span data-ttu-id="a5eff-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5eff-133">RELATED LINKS</span></span>

[<span data-ttu-id="a5eff-134">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a5eff-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a5eff-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="a5eff-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


