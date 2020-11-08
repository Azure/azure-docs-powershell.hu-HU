---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016479"
---
# <span data-ttu-id="87949-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="87949-101">Remove-AzureDns</span></span>

## <span data-ttu-id="87949-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87949-102">SYNOPSIS</span></span>
<span data-ttu-id="87949-103">DNS-kiszolgáló eltávolítása Azure-szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="87949-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="87949-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87949-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="87949-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87949-105">DESCRIPTION</span></span>
<span data-ttu-id="87949-106">A **Remove-AzureDns** parancsmag az Azure-szolgáltatásból távolítja el a DNS-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="87949-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="87949-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87949-107">EXAMPLES</span></span>

### <span data-ttu-id="87949-108">1. példa: DNS-kiszolgáló eltávolítása szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="87949-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="87949-109">Ez a parancs eltávolítja a Dns07 nevű DNS-kiszolgálót a ContosoService-ből.</span><span class="sxs-lookup"><span data-stu-id="87949-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="87949-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87949-110">PARAMETERS</span></span>

### <span data-ttu-id="87949-111">-Force</span><span class="sxs-lookup"><span data-stu-id="87949-111">-Force</span></span>
<span data-ttu-id="87949-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="87949-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87949-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="87949-113">-InformationAction</span></span>
<span data-ttu-id="87949-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="87949-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87949-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="87949-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87949-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="87949-116">Continue</span></span>
- <span data-ttu-id="87949-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="87949-117">Ignore</span></span>
- <span data-ttu-id="87949-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="87949-118">Inquire</span></span>
- <span data-ttu-id="87949-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="87949-119">SilentlyContinue</span></span>
- <span data-ttu-id="87949-120">állj</span><span class="sxs-lookup"><span data-stu-id="87949-120">Stop</span></span>
- <span data-ttu-id="87949-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="87949-121">Suspend</span></span>

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

### <span data-ttu-id="87949-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="87949-122">-InformationVariable</span></span>
<span data-ttu-id="87949-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="87949-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="87949-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87949-124">-Name</span></span>
<span data-ttu-id="87949-125">Annak a DNS-kiszolgálónak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="87949-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="87949-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="87949-126">-Profile</span></span>
<span data-ttu-id="87949-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="87949-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87949-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="87949-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87949-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="87949-129">-ServiceName</span></span>
<span data-ttu-id="87949-130">Annak a szolgáltatásnak a neve, amelyből a parancsmag eltávolítja a DNS-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="87949-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="87949-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87949-131">CommonParameters</span></span>
<span data-ttu-id="87949-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87949-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87949-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87949-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87949-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87949-134">INPUTS</span></span>

## <span data-ttu-id="87949-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87949-135">OUTPUTS</span></span>

### <span data-ttu-id="87949-136">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="87949-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="87949-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87949-137">NOTES</span></span>

## <span data-ttu-id="87949-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87949-138">RELATED LINKS</span></span>

[<span data-ttu-id="87949-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="87949-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="87949-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="87949-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="87949-141">Új – AzureDns</span><span class="sxs-lookup"><span data-stu-id="87949-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="87949-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="87949-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


