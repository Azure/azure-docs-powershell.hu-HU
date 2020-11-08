---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016475"
---
# <span data-ttu-id="80400-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80400-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="80400-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80400-102">SYNOPSIS</span></span>
<span data-ttu-id="80400-103">Belső terheléselosztó konfiguráció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="80400-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="80400-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80400-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80400-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="80400-105">DESCRIPTION</span></span>
<span data-ttu-id="80400-106">A **Remove-AzureInternalLoadBalancer** parancsmag eltávolítja a belső terheléselosztási konfigurációt egy Azure-szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="80400-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="80400-107">Ha bármely végpont jelenleg a belső terheléselosztásra hivatkozik, ez a parancsmag nem tudja eltávolítani a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="80400-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="80400-108">Példák</span><span class="sxs-lookup"><span data-stu-id="80400-108">EXAMPLES</span></span>

### <span data-ttu-id="80400-109">1. példa: belső terheléselosztó konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="80400-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="80400-110">Ez a parancs eltávolítja a ContosoService nevű szolgáltatás belső terheléselosztó konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="80400-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="80400-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80400-111">PARAMETERS</span></span>

### <span data-ttu-id="80400-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80400-112">-InformationAction</span></span>
<span data-ttu-id="80400-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="80400-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80400-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="80400-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80400-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="80400-115">Continue</span></span>
- <span data-ttu-id="80400-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="80400-116">Ignore</span></span>
- <span data-ttu-id="80400-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="80400-117">Inquire</span></span>
- <span data-ttu-id="80400-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80400-118">SilentlyContinue</span></span>
- <span data-ttu-id="80400-119">állj</span><span class="sxs-lookup"><span data-stu-id="80400-119">Stop</span></span>
- <span data-ttu-id="80400-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="80400-120">Suspend</span></span>

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

### <span data-ttu-id="80400-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80400-121">-InformationVariable</span></span>
<span data-ttu-id="80400-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="80400-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="80400-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="80400-123">-Profile</span></span>
<span data-ttu-id="80400-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="80400-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80400-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="80400-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80400-126">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="80400-126">-ServiceName</span></span>
<span data-ttu-id="80400-127">Annak a szolgáltatásnak a neve, amelyből a parancsmag eltávolítja a belső terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="80400-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="80400-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80400-128">CommonParameters</span></span>
<span data-ttu-id="80400-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80400-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80400-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80400-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80400-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80400-131">INPUTS</span></span>

## <span data-ttu-id="80400-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80400-132">OUTPUTS</span></span>

### <span data-ttu-id="80400-133">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="80400-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="80400-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80400-134">NOTES</span></span>

## <span data-ttu-id="80400-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80400-135">RELATED LINKS</span></span>

[<span data-ttu-id="80400-136">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80400-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="80400-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80400-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="80400-138">Új – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="80400-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="80400-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80400-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


