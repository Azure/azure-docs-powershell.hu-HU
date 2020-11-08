---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015734"
---
# <span data-ttu-id="95f78-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="95f78-101">Add-AzureDns</span></span>

## <span data-ttu-id="95f78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95f78-102">SYNOPSIS</span></span>
<span data-ttu-id="95f78-103">DNS-kiszolgáló felvétele Azure-szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="95f78-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="95f78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95f78-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="95f78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95f78-105">DESCRIPTION</span></span>
<span data-ttu-id="95f78-106">A **Add-AzureDns** parancsmag egy DNS-kiszolgálót ad hozzá egy Azure-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="95f78-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="95f78-107">Példák</span><span class="sxs-lookup"><span data-stu-id="95f78-107">EXAMPLES</span></span>

### <span data-ttu-id="95f78-108">1. példa: DNS-kiszolgáló felvétele</span><span class="sxs-lookup"><span data-stu-id="95f78-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="95f78-109">Ez a parancs hozzáadja azt a DNS-kiszolgálót, amely a 10.1.2.4 címet tartalmazza a ContosoService-hoz.</span><span class="sxs-lookup"><span data-stu-id="95f78-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="95f78-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95f78-110">PARAMETERS</span></span>

### <span data-ttu-id="95f78-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="95f78-111">-InformationAction</span></span>
<span data-ttu-id="95f78-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="95f78-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="95f78-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="95f78-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95f78-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="95f78-114">Continue</span></span>
- <span data-ttu-id="95f78-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="95f78-115">Ignore</span></span>
- <span data-ttu-id="95f78-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="95f78-116">Inquire</span></span>
- <span data-ttu-id="95f78-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="95f78-117">SilentlyContinue</span></span>
- <span data-ttu-id="95f78-118">állj</span><span class="sxs-lookup"><span data-stu-id="95f78-118">Stop</span></span>
- <span data-ttu-id="95f78-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="95f78-119">Suspend</span></span>

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

### <span data-ttu-id="95f78-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="95f78-120">-InformationVariable</span></span>
<span data-ttu-id="95f78-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="95f78-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="95f78-122">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="95f78-122">-IPAddress</span></span>
<span data-ttu-id="95f78-123">A DNS-kiszolgáló IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95f78-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="95f78-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95f78-124">-Name</span></span>
<span data-ttu-id="95f78-125">A DNS-kiszolgáló felhasználóbarát nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95f78-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="95f78-126">Ez a név nem feltétlenül teljesen minősített tartománynév.</span><span class="sxs-lookup"><span data-stu-id="95f78-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="95f78-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="95f78-127">-Profile</span></span>
<span data-ttu-id="95f78-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="95f78-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95f78-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="95f78-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95f78-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="95f78-130">-ServiceName</span></span>
<span data-ttu-id="95f78-131">Annak a szolgáltatásnak a nevét adja meg, amelyre a parancsmag hozzáadja a DNS-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="95f78-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f78-132">CommonParameters</span></span>
<span data-ttu-id="95f78-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95f78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f78-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f78-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f78-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95f78-135">INPUTS</span></span>

## <span data-ttu-id="95f78-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95f78-136">OUTPUTS</span></span>

### <span data-ttu-id="95f78-137">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="95f78-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="95f78-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95f78-138">NOTES</span></span>

## <span data-ttu-id="95f78-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95f78-139">RELATED LINKS</span></span>

[<span data-ttu-id="95f78-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="95f78-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="95f78-141">Új – AzureDns</span><span class="sxs-lookup"><span data-stu-id="95f78-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="95f78-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="95f78-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="95f78-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="95f78-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


