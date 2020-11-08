---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015713"
---
# <span data-ttu-id="56a53-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="56a53-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="56a53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56a53-102">SYNOPSIS</span></span>
<span data-ttu-id="56a53-103">Virtuális IP-címet ad hozzá egy felhőalapú szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="56a53-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="56a53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56a53-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="56a53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56a53-105">DESCRIPTION</span></span>
<span data-ttu-id="56a53-106">Az **Add-AzureVirtualIP** parancsmag új virtuális IP-címet (VIP) ad hozzá az Azure-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="56a53-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="56a53-107">Az új virtuális IP-cím névvel rendelkezik, de az IP-cím nincs kiosztva.</span><span class="sxs-lookup"><span data-stu-id="56a53-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="56a53-108">Az IP-cím csak akkor lesz kiosztva, ha végpontot társít a VIP-hez.</span><span class="sxs-lookup"><span data-stu-id="56a53-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="56a53-109">További részletekért tekintse meg a Add-AzureEndpointt.</span><span class="sxs-lookup"><span data-stu-id="56a53-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="56a53-110">Előfizetése csak akkor terheli meg a plusz VIP-t, ha egy végponthoz társítva van.</span><span class="sxs-lookup"><span data-stu-id="56a53-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="56a53-111">Példák</span><span class="sxs-lookup"><span data-stu-id="56a53-111">EXAMPLES</span></span>

### <span data-ttu-id="56a53-112">1. példa: virtuális IP hozzáadása szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="56a53-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="56a53-113">Ez a parancs egy virtuális IP-címet ad hozzá a szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="56a53-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="56a53-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56a53-114">PARAMETERS</span></span>

### <span data-ttu-id="56a53-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="56a53-115">-InformationAction</span></span>
<span data-ttu-id="56a53-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="56a53-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56a53-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="56a53-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56a53-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="56a53-118">Continue</span></span>
- <span data-ttu-id="56a53-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="56a53-119">Ignore</span></span>
- <span data-ttu-id="56a53-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="56a53-120">Inquire</span></span>
- <span data-ttu-id="56a53-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56a53-121">SilentlyContinue</span></span>
- <span data-ttu-id="56a53-122">állj</span><span class="sxs-lookup"><span data-stu-id="56a53-122">Stop</span></span>
- <span data-ttu-id="56a53-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="56a53-123">Suspend</span></span>

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

### <span data-ttu-id="56a53-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56a53-124">-InformationVariable</span></span>
<span data-ttu-id="56a53-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="56a53-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="56a53-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="56a53-126">-Profile</span></span>
<span data-ttu-id="56a53-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="56a53-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56a53-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="56a53-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56a53-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="56a53-129">-ServiceName</span></span>
<span data-ttu-id="56a53-130">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56a53-130">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="56a53-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="56a53-131">-VirtualIPName</span></span>
<span data-ttu-id="56a53-132">A virtuális IP-cím nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56a53-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a53-133">CommonParameters</span></span>
<span data-ttu-id="56a53-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56a53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a53-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56a53-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a53-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56a53-136">INPUTS</span></span>

## <span data-ttu-id="56a53-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56a53-137">OUTPUTS</span></span>

### <span data-ttu-id="56a53-138">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="56a53-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="56a53-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56a53-139">NOTES</span></span>

## <span data-ttu-id="56a53-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56a53-140">RELATED LINKS</span></span>

[<span data-ttu-id="56a53-141">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a53-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="56a53-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="56a53-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


