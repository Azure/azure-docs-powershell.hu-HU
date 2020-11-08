---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016288"
---
# <span data-ttu-id="f15ad-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="f15ad-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="f15ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f15ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f15ad-103">A jelenlegi előfizetésből kapja meg az Azure virtuális hálózat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f15ad-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="f15ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f15ad-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f15ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f15ad-105">DESCRIPTION</span></span>
<span data-ttu-id="f15ad-106">A **Get-AzureVNetConfig** parancsmag lekéri az aktuális Azure-előfizetés virtuális hálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f15ad-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="f15ad-107">Ha a *ExportToFile* paramétert adja meg, létrejön egy hálózati konfigurációs fájl.</span><span class="sxs-lookup"><span data-stu-id="f15ad-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="f15ad-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f15ad-108">EXAMPLES</span></span>

### <span data-ttu-id="f15ad-109">Példa 1: a jelenlegi Azure-előfizetés virtuális hálózati konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f15ad-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="f15ad-110">Ez a parancs az aktuális Azure-előfizetés virtuális hálózati konfigurációját kapja, és megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="f15ad-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="f15ad-111">2. példa: az aktuális Azure-előfizetés virtuális hálózati konfigurációjának beszerzése és helyi fájlba mentése</span><span class="sxs-lookup"><span data-stu-id="f15ad-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="f15ad-112">Ez a parancs beolvassa az aktuális Azure-előfizetés virtuális hálózati konfigurációját, majd egy helyi fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="f15ad-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="f15ad-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f15ad-113">PARAMETERS</span></span>

### <span data-ttu-id="f15ad-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="f15ad-114">-ExportToFile</span></span>
<span data-ttu-id="f15ad-115">A beállításokból létrehozandó hálózati konfigurációs fájl elérési útját és fájlnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f15ad-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15ad-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f15ad-116">-InformationAction</span></span>
<span data-ttu-id="f15ad-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f15ad-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f15ad-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f15ad-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f15ad-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f15ad-119">Continue</span></span>
- <span data-ttu-id="f15ad-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f15ad-120">Ignore</span></span>
- <span data-ttu-id="f15ad-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f15ad-121">Inquire</span></span>
- <span data-ttu-id="f15ad-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f15ad-122">SilentlyContinue</span></span>
- <span data-ttu-id="f15ad-123">állj</span><span class="sxs-lookup"><span data-stu-id="f15ad-123">Stop</span></span>
- <span data-ttu-id="f15ad-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f15ad-124">Suspend</span></span>

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

### <span data-ttu-id="f15ad-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f15ad-125">-InformationVariable</span></span>
<span data-ttu-id="f15ad-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f15ad-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f15ad-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="f15ad-127">-Profile</span></span>
<span data-ttu-id="f15ad-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f15ad-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f15ad-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f15ad-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f15ad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15ad-130">CommonParameters</span></span>
<span data-ttu-id="f15ad-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f15ad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15ad-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15ad-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15ad-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f15ad-133">INPUTS</span></span>

## <span data-ttu-id="f15ad-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f15ad-134">OUTPUTS</span></span>

## <span data-ttu-id="f15ad-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f15ad-135">NOTES</span></span>

## <span data-ttu-id="f15ad-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f15ad-136">RELATED LINKS</span></span>

[<span data-ttu-id="f15ad-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="f15ad-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="f15ad-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="f15ad-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="f15ad-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="f15ad-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


