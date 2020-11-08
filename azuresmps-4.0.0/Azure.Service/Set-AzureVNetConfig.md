---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015787"
---
# <span data-ttu-id="704ac-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="704ac-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="704ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="704ac-102">SYNOPSIS</span></span>
<span data-ttu-id="704ac-103">Az Azure Cloud-szolgáltatás virtuális hálózati beállításainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="704ac-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="704ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="704ac-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="704ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="704ac-105">DESCRIPTION</span></span>
<span data-ttu-id="704ac-106">A **set-AzureVNetConfig** parancsmag frissíti az aktuális Azure-előfizetés hálózati konfigurációját a hálózati konfigurációs fájl (. netcfg) elérési útjának megadásával.</span><span class="sxs-lookup"><span data-stu-id="704ac-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="704ac-107">A hálózati konfigurációs fájl a felhőalapú szolgáltatásokhoz tartozó DNS-kiszolgálókat és alhálózatokat definiálja az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="704ac-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="704ac-108">Példák</span><span class="sxs-lookup"><span data-stu-id="704ac-108">EXAMPLES</span></span>

### <span data-ttu-id="704ac-109">Példa 1: az Azure-előfizetés hálózati konfigurációjának frissítése helyi fájlra</span><span class="sxs-lookup"><span data-stu-id="704ac-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="704ac-110">Ez a parancs frissíti az aktuális Microsoft Azure-előfizetés hálózati konfigurációját a "c:\temp\MyAzNets.netcfg" helyi fájlban.</span><span class="sxs-lookup"><span data-stu-id="704ac-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="704ac-111">2. példa: az Azure-előfizetés beállítása, majd a hálózati konfiguráció frissítése</span><span class="sxs-lookup"><span data-stu-id="704ac-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="704ac-112">Ez a példa beállítja a Microsoft Azure-előfizetést, majd frissíti az előfizetés hálózati konfigurációját a "c:\temp\MyAzNets.netcfg" helyi fájlban definiált konfiguráció használatával.</span><span class="sxs-lookup"><span data-stu-id="704ac-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="704ac-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="704ac-113">PARAMETERS</span></span>

### <span data-ttu-id="704ac-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="704ac-114">-ConfigurationPath</span></span>
<span data-ttu-id="704ac-115">A hálózati konfigurációs fájlok (. netcfg) elérési útját és fájlnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="704ac-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="704ac-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="704ac-116">-InformationAction</span></span>
<span data-ttu-id="704ac-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="704ac-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="704ac-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="704ac-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="704ac-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="704ac-119">Continue</span></span>
- <span data-ttu-id="704ac-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="704ac-120">Ignore</span></span>
- <span data-ttu-id="704ac-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="704ac-121">Inquire</span></span>
- <span data-ttu-id="704ac-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="704ac-122">SilentlyContinue</span></span>
- <span data-ttu-id="704ac-123">állj</span><span class="sxs-lookup"><span data-stu-id="704ac-123">Stop</span></span>
- <span data-ttu-id="704ac-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="704ac-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="704ac-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="704ac-125">-InformationVariable</span></span>
<span data-ttu-id="704ac-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="704ac-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="704ac-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="704ac-127">-Profile</span></span>
<span data-ttu-id="704ac-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="704ac-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="704ac-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="704ac-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="704ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704ac-130">CommonParameters</span></span>
<span data-ttu-id="704ac-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="704ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704ac-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704ac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704ac-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="704ac-133">INPUTS</span></span>

## <span data-ttu-id="704ac-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="704ac-134">OUTPUTS</span></span>

## <span data-ttu-id="704ac-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="704ac-135">NOTES</span></span>

## <span data-ttu-id="704ac-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="704ac-136">RELATED LINKS</span></span>

[<span data-ttu-id="704ac-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="704ac-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="704ac-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="704ac-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="704ac-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="704ac-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


