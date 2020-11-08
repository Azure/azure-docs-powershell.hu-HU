---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015625"
---
# <span data-ttu-id="ba37c-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="ba37c-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="ba37c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba37c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba37c-103">Beolvassa az Azure RemoteApp VPN-eszközök konfigurációs parancsfájlját.</span><span class="sxs-lookup"><span data-stu-id="ba37c-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="ba37c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba37c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ba37c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba37c-105">DESCRIPTION</span></span>
<span data-ttu-id="ba37c-106">A **Get-AzureRemoteAppVpnDeviceConfigScript** parancsmag beolvassa az Azure RemoteApp virtual private Network (VPN) eszközök konfigurációs parancsfájlját.</span><span class="sxs-lookup"><span data-stu-id="ba37c-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="ba37c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba37c-107">EXAMPLES</span></span>

### <span data-ttu-id="ba37c-108">Példa 1: konfigurációs parancsfájl beszerzése VPN-eszközön</span><span class="sxs-lookup"><span data-stu-id="ba37c-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="ba37c-109">Ez a parancs azt a parancsfájl-vagy konfigurációs fájlt adja eredményül, amely a ContosoVNet nevű virtuális hálózat VPN-eszközének konfigurálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="ba37c-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="ba37c-110">Ezt a parancsfájl-vagy konfigurációs fájlt a megfelelő módon kell futtatni vagy betölteni a VPN-eszközre.</span><span class="sxs-lookup"><span data-stu-id="ba37c-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="ba37c-111">Tekintse meg az egyes eszközökre vonatkozó egyedi követelményeket a VPN-eszköz forgalmazójától.</span><span class="sxs-lookup"><span data-stu-id="ba37c-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="ba37c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba37c-112">PARAMETERS</span></span>

### <span data-ttu-id="ba37c-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="ba37c-113">-OSFamily</span></span>
<span data-ttu-id="ba37c-114">Annak az operációs rendszernek a családját adja meg, amely az eszköz platformján fut.</span><span class="sxs-lookup"><span data-stu-id="ba37c-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba37c-115">-Platform</span><span class="sxs-lookup"><span data-stu-id="ba37c-115">-Platform</span></span>
<span data-ttu-id="ba37c-116">Az eszköz platformját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba37c-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba37c-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ba37c-117">-Profile</span></span>
<span data-ttu-id="ba37c-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ba37c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba37c-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ba37c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba37c-120">-Vendor</span><span class="sxs-lookup"><span data-stu-id="ba37c-120">-Vendor</span></span>
<span data-ttu-id="ba37c-121">A VPN-eszköz szállítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba37c-121">Specifies the vendor of the VPN device.</span></span>

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

### <span data-ttu-id="ba37c-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ba37c-122">-VNetName</span></span>
<span data-ttu-id="ba37c-123">Egy Azure RemoteApp virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba37c-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba37c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba37c-124">CommonParameters</span></span>
<span data-ttu-id="ba37c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba37c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba37c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba37c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba37c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba37c-127">INPUTS</span></span>

## <span data-ttu-id="ba37c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba37c-128">OUTPUTS</span></span>

## <span data-ttu-id="ba37c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba37c-129">NOTES</span></span>

## <span data-ttu-id="ba37c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba37c-130">RELATED LINKS</span></span>

[<span data-ttu-id="ba37c-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="ba37c-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


