---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015492"
---
# <span data-ttu-id="dea44-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="dea44-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="dea44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dea44-102">SYNOPSIS</span></span>
<span data-ttu-id="dea44-103">Törli a hálózati konfigurációt az aktuális Azure-előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="dea44-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="dea44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dea44-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dea44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dea44-105">DESCRIPTION</span></span>
<span data-ttu-id="dea44-106">A **Remove-AzureVNetConfig** parancsmag az aktuális Azure-előfizetésből eltávolítja az összes virtuális hálózati beállítást.</span><span class="sxs-lookup"><span data-stu-id="dea44-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="dea44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dea44-107">EXAMPLES</span></span>

### <span data-ttu-id="dea44-108">1. példa: virtuális hálózati konfiguráció eltávolítása a jelenlegi előfizetésből</span><span class="sxs-lookup"><span data-stu-id="dea44-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="dea44-109">Ez a parancs eltávolítja a virtuális hálózati konfigurációt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="dea44-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="dea44-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dea44-110">PARAMETERS</span></span>

### <span data-ttu-id="dea44-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dea44-111">-InformationAction</span></span>
<span data-ttu-id="dea44-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="dea44-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dea44-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dea44-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dea44-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="dea44-114">Continue</span></span>
- <span data-ttu-id="dea44-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="dea44-115">Ignore</span></span>
- <span data-ttu-id="dea44-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="dea44-116">Inquire</span></span>
- <span data-ttu-id="dea44-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dea44-117">SilentlyContinue</span></span>
- <span data-ttu-id="dea44-118">állj</span><span class="sxs-lookup"><span data-stu-id="dea44-118">Stop</span></span>
- <span data-ttu-id="dea44-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="dea44-119">Suspend</span></span>

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

### <span data-ttu-id="dea44-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dea44-120">-InformationVariable</span></span>
<span data-ttu-id="dea44-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="dea44-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dea44-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="dea44-122">-Profile</span></span>
<span data-ttu-id="dea44-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="dea44-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dea44-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="dea44-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dea44-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea44-125">CommonParameters</span></span>
<span data-ttu-id="dea44-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dea44-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea44-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea44-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea44-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea44-128">INPUTS</span></span>

## <span data-ttu-id="dea44-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea44-129">OUTPUTS</span></span>

## <span data-ttu-id="dea44-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dea44-130">NOTES</span></span>

## <span data-ttu-id="dea44-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dea44-131">RELATED LINKS</span></span>

[<span data-ttu-id="dea44-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="dea44-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="dea44-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="dea44-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="dea44-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="dea44-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


