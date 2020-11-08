---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015646"
---
# <span data-ttu-id="6886c-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6886c-101">Get-AzureDns</span></span>

## <span data-ttu-id="6886c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6886c-102">SYNOPSIS</span></span>
<span data-ttu-id="6886c-103">Beolvassa az Azure-alapú központi környezet DNS-beállításait.</span><span class="sxs-lookup"><span data-stu-id="6886c-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="6886c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6886c-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6886c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6886c-105">DESCRIPTION</span></span>
<span data-ttu-id="6886c-106">A **Get-AzureDns** parancsmag az Azure-alapú központi telepítéséhez szükséges DNS-beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6886c-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="6886c-107">A parancsmag a DNS-kiszolgáló rövid nevét és IP-címét adja eredményül egy DNS-beállítási objektumban.</span><span class="sxs-lookup"><span data-stu-id="6886c-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="6886c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6886c-108">EXAMPLES</span></span>

### <span data-ttu-id="6886c-109">Példa 1: DNS-beállítások beszerzése</span><span class="sxs-lookup"><span data-stu-id="6886c-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="6886c-110">Ez a parancs a **Get-AzureDeployment** parancsmagot használja a ContosoService nevű szolgáltatás termelésének beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="6886c-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="6886c-111">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="6886c-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6886c-112">Az aktuális parancsmag a DNS-beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6886c-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="6886c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6886c-113">PARAMETERS</span></span>

### <span data-ttu-id="6886c-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="6886c-114">-DnsSettings</span></span>
<span data-ttu-id="6886c-115">Egy **DnsSettings** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6886c-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6886c-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6886c-116">-InformationAction</span></span>
<span data-ttu-id="6886c-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="6886c-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6886c-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6886c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6886c-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="6886c-119">Continue</span></span>
- <span data-ttu-id="6886c-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="6886c-120">Ignore</span></span>
- <span data-ttu-id="6886c-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="6886c-121">Inquire</span></span>
- <span data-ttu-id="6886c-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6886c-122">SilentlyContinue</span></span>
- <span data-ttu-id="6886c-123">állj</span><span class="sxs-lookup"><span data-stu-id="6886c-123">Stop</span></span>
- <span data-ttu-id="6886c-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="6886c-124">Suspend</span></span>

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

### <span data-ttu-id="6886c-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6886c-125">-InformationVariable</span></span>
<span data-ttu-id="6886c-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="6886c-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6886c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6886c-127">CommonParameters</span></span>
<span data-ttu-id="6886c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6886c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6886c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6886c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6886c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6886c-130">INPUTS</span></span>

## <span data-ttu-id="6886c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6886c-131">OUTPUTS</span></span>

## <span data-ttu-id="6886c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6886c-132">NOTES</span></span>

## <span data-ttu-id="6886c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6886c-133">RELATED LINKS</span></span>

[<span data-ttu-id="6886c-134">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6886c-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="6886c-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6886c-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="6886c-136">Új – AzureDns</span><span class="sxs-lookup"><span data-stu-id="6886c-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="6886c-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6886c-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="6886c-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6886c-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


