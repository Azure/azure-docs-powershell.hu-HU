---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015487"
---
# <span data-ttu-id="d2c31-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="d2c31-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="d2c31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2c31-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c31-103">Virtuális IP-cím törlése a felhőalapú szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="d2c31-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="d2c31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2c31-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d2c31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2c31-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c31-106">A **Remove-AzureVirtualIP** parancsmag egy virtuális IP-címet (VIP) töröl egy Azure-szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="d2c31-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="d2c31-107">A művelet csak akkor sikerül, ha a virtuális IP-hez nincs végpont társítva.</span><span class="sxs-lookup"><span data-stu-id="d2c31-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="d2c31-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d2c31-108">EXAMPLES</span></span>

### <span data-ttu-id="d2c31-109">1. példa: virtuális IP-cím eltávolítása egy szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="d2c31-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="d2c31-110">Ez a parancs eltávolítja a virtuális IP-címet egy szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="d2c31-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="d2c31-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2c31-111">PARAMETERS</span></span>

### <span data-ttu-id="d2c31-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d2c31-112">-Force</span></span>
<span data-ttu-id="d2c31-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d2c31-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c31-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d2c31-114">-InformationAction</span></span>
<span data-ttu-id="d2c31-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="d2c31-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d2c31-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d2c31-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2c31-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="d2c31-117">Continue</span></span>
- <span data-ttu-id="d2c31-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="d2c31-118">Ignore</span></span>
- <span data-ttu-id="d2c31-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="d2c31-119">Inquire</span></span>
- <span data-ttu-id="d2c31-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d2c31-120">SilentlyContinue</span></span>
- <span data-ttu-id="d2c31-121">állj</span><span class="sxs-lookup"><span data-stu-id="d2c31-121">Stop</span></span>
- <span data-ttu-id="d2c31-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="d2c31-122">Suspend</span></span>

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

### <span data-ttu-id="d2c31-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d2c31-123">-InformationVariable</span></span>
<span data-ttu-id="d2c31-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d2c31-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d2c31-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d2c31-125">-Profile</span></span>
<span data-ttu-id="d2c31-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d2c31-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2c31-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d2c31-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2c31-128">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="d2c31-128">-ServiceName</span></span>
<span data-ttu-id="d2c31-129">Annak a szolgáltatásnak a nevét adja meg, amelyből el szeretné távolítani a virtuális IP-címet.</span><span class="sxs-lookup"><span data-stu-id="d2c31-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

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

### <span data-ttu-id="d2c31-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="d2c31-130">-VirtualIPName</span></span>
<span data-ttu-id="d2c31-131">Annak a virtuális IP-címnek a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="d2c31-131">Specifies the name of the virtual IP address to remove.</span></span>

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

### <span data-ttu-id="d2c31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c31-132">CommonParameters</span></span>
<span data-ttu-id="d2c31-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2c31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c31-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c31-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c31-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2c31-135">INPUTS</span></span>

## <span data-ttu-id="d2c31-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2c31-136">OUTPUTS</span></span>

### <span data-ttu-id="d2c31-137">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="d2c31-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="d2c31-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2c31-138">NOTES</span></span>

## <span data-ttu-id="d2c31-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2c31-139">RELATED LINKS</span></span>

[<span data-ttu-id="d2c31-140">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="d2c31-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


