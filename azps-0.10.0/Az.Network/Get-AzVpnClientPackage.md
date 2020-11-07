---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841474"
---
# <span data-ttu-id="45260-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="45260-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="45260-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45260-102">SYNOPSIS</span></span>
<span data-ttu-id="45260-103">Információt kap a VPN-ügyfél csomagról.</span><span class="sxs-lookup"><span data-stu-id="45260-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="45260-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45260-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45260-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45260-105">DESCRIPTION</span></span>
<span data-ttu-id="45260-106">A **Get-AzVpnClientPackage** parancsmag információt kap a virtuális hálózati átjáróból elérhető VPN-ügyfél-csomagokról.</span><span class="sxs-lookup"><span data-stu-id="45260-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="45260-107">Az ügyfél csomagjai olyan konfigurációs adatokat tartalmaznak, amelyek lehetővé teszik, hogy egy ügyfélszámítógép virtuális MAGÁNHÁLÓZATI kapcsolatot hozzon létre egy Azure virtuális hálózattal; a VPN-kapcsolat létrehozásához az ügyfélgépeknek telepítve kell lenniük a megfelelő konfigurációs csomagnak.</span><span class="sxs-lookup"><span data-stu-id="45260-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="45260-108">Az ügyfélszámítógép Windows-verziójának (például a Windows 7 vagy a Windows 10) és az ügyfélszámítógép processzor-architektúrájának (AMD64 vagy x86) alapján is elérhetők a különféle konfigurációs csomagok.</span><span class="sxs-lookup"><span data-stu-id="45260-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="45260-109">A **Get-AzVpnClientPackage** futtatásakor meg kell adnia az architektúra típusát.</span><span class="sxs-lookup"><span data-stu-id="45260-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="45260-110">Példák</span><span class="sxs-lookup"><span data-stu-id="45260-110">EXAMPLES</span></span>

### <span data-ttu-id="45260-111">1. példa: adatok beszerzése a processzor-architektúra VPN-csomagról</span><span class="sxs-lookup"><span data-stu-id="45260-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="45260-112">Ez a parancs információt kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróban tárolt AMD64 VPN-csomagokról.</span><span class="sxs-lookup"><span data-stu-id="45260-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="45260-113">Ha információkat szeretne kapni az x86-os ügyfél-csomagokról, állítsa az *ProcessorArchitecture* paraméter értékét x86 értékre.</span><span class="sxs-lookup"><span data-stu-id="45260-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="45260-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45260-114">PARAMETERS</span></span>

### <span data-ttu-id="45260-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45260-115">-DefaultProfile</span></span>
<span data-ttu-id="45260-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45260-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45260-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="45260-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="45260-118">Annak a CPU-architektúrának a típusát adja meg, amelyre az ügyfél-csomag van tervezve.</span><span class="sxs-lookup"><span data-stu-id="45260-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="45260-119">Az érvényes értékek az Amd64 és az x86.</span><span class="sxs-lookup"><span data-stu-id="45260-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45260-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45260-120">-ResourceGroupName</span></span>
<span data-ttu-id="45260-121">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="45260-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="45260-122">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="45260-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45260-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="45260-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="45260-124">Annak a virtuális hálózati átjárónak a neve, amelybe az ügyfél-csomag adatai vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="45260-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45260-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45260-125">CommonParameters</span></span>
<span data-ttu-id="45260-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45260-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45260-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45260-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45260-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45260-128">INPUTS</span></span>

### <span data-ttu-id="45260-129">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="45260-129">String</span></span>
<span data-ttu-id="45260-130">A ' ResourceGroupName ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="45260-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="45260-131">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="45260-131">String</span></span>
<span data-ttu-id="45260-132">A ' VirtualNetworkGatewayName ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="45260-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="45260-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45260-133">OUTPUTS</span></span>

###  
<span data-ttu-id="45260-134">A **Get-AzVpnClientPackage** a System. String objektum példányait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="45260-134">**Get-AzVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="45260-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45260-135">NOTES</span></span>

## <span data-ttu-id="45260-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45260-136">RELATED LINKS</span></span>

[<span data-ttu-id="45260-137">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="45260-137">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="45260-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="45260-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


