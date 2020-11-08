---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016069"
---
# <span data-ttu-id="75367-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="75367-101">Set-AzureDns</span></span>

## <span data-ttu-id="75367-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75367-102">SYNOPSIS</span></span>
<span data-ttu-id="75367-103">Módosítja egy DNS-kiszolgáló IP-címét.</span><span class="sxs-lookup"><span data-stu-id="75367-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="75367-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75367-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="75367-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75367-105">DESCRIPTION</span></span>
<span data-ttu-id="75367-106">A **set-AzureDns** parancsmag egy Azure-szolgáltatás DNS-kiszolgálójának IP-címét módosítja.</span><span class="sxs-lookup"><span data-stu-id="75367-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="75367-107">Példák</span><span class="sxs-lookup"><span data-stu-id="75367-107">EXAMPLES</span></span>

### <span data-ttu-id="75367-108">Példa 1: a DNS-kiszolgáló IP-címének módosítása</span><span class="sxs-lookup"><span data-stu-id="75367-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="75367-109">Ez a parancs módosítja a Dns07 nevű DNS-kiszolgáló IP-címét a ContosoService nevű szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="75367-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="75367-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75367-110">PARAMETERS</span></span>

### <span data-ttu-id="75367-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="75367-111">-InformationAction</span></span>
<span data-ttu-id="75367-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="75367-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="75367-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="75367-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75367-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="75367-114">Continue</span></span>
- <span data-ttu-id="75367-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="75367-115">Ignore</span></span>
- <span data-ttu-id="75367-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="75367-116">Inquire</span></span>
- <span data-ttu-id="75367-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="75367-117">SilentlyContinue</span></span>
- <span data-ttu-id="75367-118">állj</span><span class="sxs-lookup"><span data-stu-id="75367-118">Stop</span></span>
- <span data-ttu-id="75367-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="75367-119">Suspend</span></span>

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

### <span data-ttu-id="75367-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="75367-120">-InformationVariable</span></span>
<span data-ttu-id="75367-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="75367-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="75367-122">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="75367-122">-IPAddress</span></span>
<span data-ttu-id="75367-123">A DNS-kiszolgáló új IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75367-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="75367-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75367-124">-Name</span></span>
<span data-ttu-id="75367-125">Annak a DNS-kiszolgálónak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="75367-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="75367-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="75367-126">-Profile</span></span>
<span data-ttu-id="75367-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="75367-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75367-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="75367-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75367-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="75367-129">-ServiceName</span></span>
<span data-ttu-id="75367-130">Annak a szolgáltatásnak a nevét adja meg, amelyre a parancsmag módosította a DNS-kiszolgáló címét.</span><span class="sxs-lookup"><span data-stu-id="75367-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="75367-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75367-131">CommonParameters</span></span>
<span data-ttu-id="75367-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75367-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75367-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75367-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75367-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75367-134">INPUTS</span></span>

## <span data-ttu-id="75367-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75367-135">OUTPUTS</span></span>

### <span data-ttu-id="75367-136">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="75367-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="75367-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75367-137">NOTES</span></span>

## <span data-ttu-id="75367-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75367-138">RELATED LINKS</span></span>

[<span data-ttu-id="75367-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="75367-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="75367-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="75367-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="75367-141">Új – AzureDns</span><span class="sxs-lookup"><span data-stu-id="75367-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="75367-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="75367-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


