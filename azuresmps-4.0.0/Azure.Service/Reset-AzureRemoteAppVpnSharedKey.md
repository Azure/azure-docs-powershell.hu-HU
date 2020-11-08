---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015471"
---
# <span data-ttu-id="7d8f5-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="7d8f5-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="7d8f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8f5-103">Az Azure RemoteApp VPN megosztott kulcsának alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="7d8f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d8f5-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d8f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d8f5-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8f5-106">A **reset-AzureRemoteAppVpnSharedKey** parancsmag visszaállítja az Azure RemoteApp virtual private Network (VPN) megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="7d8f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7d8f5-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8f5-108">1. példa: virtuális hálózat megosztott kulcsának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="7d8f5-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="7d8f5-109">Ez a parancs visszaállítja a ContosoVNet nevű virtuális hálózat megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="7d8f5-110">A helyszíni hálózat VPN-kapcsolata offline állapotban marad mindaddig, amíg az új megosztott kulcs nincs konfigurálva a VPN-eszközön.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="7d8f5-111">A VPN-eszköz konfigurálásához a **Get-AzureRemoteAppVpnDeviceConfigScript** parancsmaggal megkeresheti a megfelelő parancsfájl-vagy konfigurációs fájlt a VPN-eszközön, majd betölthet egy parancsfájlt vagy konfigurációs fájlt a VPN-eszközre.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="7d8f5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d8f5-112">PARAMETERS</span></span>

### <span data-ttu-id="7d8f5-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="7d8f5-113">-Profile</span></span>
<span data-ttu-id="7d8f5-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d8f5-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f5-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="7d8f5-116">-VNetName</span></span>
<span data-ttu-id="7d8f5-117">Az Azure RemoteApp virtuális hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f5-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d8f5-118">-Confirm</span></span>
<span data-ttu-id="7d8f5-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8f5-120">-WhatIf</span></span>
<span data-ttu-id="7d8f5-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8f5-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8f5-123">CommonParameters</span></span>
<span data-ttu-id="7d8f5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d8f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8f5-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8f5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8f5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d8f5-126">INPUTS</span></span>

## <span data-ttu-id="7d8f5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d8f5-127">OUTPUTS</span></span>

### <span data-ttu-id="7d8f5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7d8f5-128">System.String</span></span>

## <span data-ttu-id="7d8f5-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d8f5-129">NOTES</span></span>

## <span data-ttu-id="7d8f5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d8f5-130">RELATED LINKS</span></span>

[<span data-ttu-id="7d8f5-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="7d8f5-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="7d8f5-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="7d8f5-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


