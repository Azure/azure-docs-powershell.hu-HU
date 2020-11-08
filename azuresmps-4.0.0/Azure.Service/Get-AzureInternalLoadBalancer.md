---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016340"
---
# <span data-ttu-id="29708-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29708-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="29708-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29708-102">SYNOPSIS</span></span>
<span data-ttu-id="29708-103">A belső terheléselosztó konfiguráció részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29708-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="29708-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29708-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="29708-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29708-105">DESCRIPTION</span></span>
<span data-ttu-id="29708-106">A **Get-AzureInternalLoadBalancer** parancsmag az Azure-szolgáltatások belső terheléselosztási konfigurációjának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29708-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="29708-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29708-107">EXAMPLES</span></span>

### <span data-ttu-id="29708-108">Példa 1: adatok beszerzése belső terheléselosztó rendszerhez</span><span class="sxs-lookup"><span data-stu-id="29708-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="29708-109">Ez a parancs a ContosoService nevű szolgáltatást a **Get-AzureService** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="29708-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="29708-110">A parancs a csővezeték-kezelő segítségével átadja ezt a szolgáltatást az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="29708-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="29708-111">Az aktuális parancsmag részletesen részletezi a szolgáltatás belső terheléselosztását.</span><span class="sxs-lookup"><span data-stu-id="29708-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="29708-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29708-112">PARAMETERS</span></span>

### <span data-ttu-id="29708-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="29708-113">-InformationAction</span></span>
<span data-ttu-id="29708-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="29708-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="29708-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="29708-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29708-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="29708-116">Continue</span></span>
- <span data-ttu-id="29708-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="29708-117">Ignore</span></span>
- <span data-ttu-id="29708-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="29708-118">Inquire</span></span>
- <span data-ttu-id="29708-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="29708-119">SilentlyContinue</span></span>
- <span data-ttu-id="29708-120">állj</span><span class="sxs-lookup"><span data-stu-id="29708-120">Stop</span></span>
- <span data-ttu-id="29708-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="29708-121">Suspend</span></span>

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

### <span data-ttu-id="29708-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="29708-122">-InformationVariable</span></span>
<span data-ttu-id="29708-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="29708-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="29708-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="29708-124">-Profile</span></span>
<span data-ttu-id="29708-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="29708-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29708-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="29708-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29708-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="29708-127">-ServiceName</span></span>
<span data-ttu-id="29708-128">Annak a szolgáltatásnak a nevét adja meg, amelyhez ez a parancsmag részletezni kíván egy belső terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="29708-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29708-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29708-129">CommonParameters</span></span>
<span data-ttu-id="29708-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29708-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29708-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29708-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29708-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29708-132">INPUTS</span></span>

## <span data-ttu-id="29708-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29708-133">OUTPUTS</span></span>

### <span data-ttu-id="29708-134">Microsoft. WindowsAzure. Command. ServiceManagement. Model. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="29708-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="29708-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29708-135">NOTES</span></span>

## <span data-ttu-id="29708-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29708-136">RELATED LINKS</span></span>

[<span data-ttu-id="29708-137">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29708-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="29708-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="29708-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="29708-139">Új – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="29708-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="29708-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29708-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="29708-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29708-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


