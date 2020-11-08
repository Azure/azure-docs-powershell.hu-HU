---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016244"
---
# <span data-ttu-id="4e198-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4e198-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="4e198-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e198-102">SYNOPSIS</span></span>
<span data-ttu-id="4e198-103">A termelés és a megállóhelyek bevezetésének felcserélése</span><span class="sxs-lookup"><span data-stu-id="4e198-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="4e198-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e198-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4e198-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e198-105">DESCRIPTION</span></span>
<span data-ttu-id="4e198-106">A **Move-AzureDeployment** parancsmag a bevezetések virtuális IP-címét a termelés és az átmeneti környezetekben cseréli.</span><span class="sxs-lookup"><span data-stu-id="4e198-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="4e198-107">Ez a parancsmag egy olyan üzembe állítást cserél, amely jelenleg az átmeneti környezetben fut a termelési környezetbe, valamint egy olyan üzembe állítást, amely a termelési környezetben fut az átmeneti környezetben.</span><span class="sxs-lookup"><span data-stu-id="4e198-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="4e198-108">Ha a bevezetést a bevezetési környezetben telepítette, és nem működik a környezet, a parancsmag a bevezetést a termelésbe helyezi.</span><span class="sxs-lookup"><span data-stu-id="4e198-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="4e198-109">Ha van egy központi telepítési környezet, és nincs bevezetése az átmeneti környezetben, a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="4e198-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="4e198-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4e198-110">EXAMPLES</span></span>

### <span data-ttu-id="4e198-111">1. példa: szolgáltatások bevezetésének cseréje</span><span class="sxs-lookup"><span data-stu-id="4e198-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="4e198-112">Ez a parancs a ContosoService nevű szolgáltatás üzembe helyezését a termelés és az átmeneti környezetek között cseréli.</span><span class="sxs-lookup"><span data-stu-id="4e198-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="4e198-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e198-113">PARAMETERS</span></span>

### <span data-ttu-id="4e198-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4e198-114">-InformationAction</span></span>
<span data-ttu-id="4e198-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="4e198-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4e198-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4e198-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e198-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="4e198-117">Continue</span></span>
- <span data-ttu-id="4e198-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="4e198-118">Ignore</span></span>
- <span data-ttu-id="4e198-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="4e198-119">Inquire</span></span>
- <span data-ttu-id="4e198-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4e198-120">SilentlyContinue</span></span>
- <span data-ttu-id="4e198-121">állj</span><span class="sxs-lookup"><span data-stu-id="4e198-121">Stop</span></span>
- <span data-ttu-id="4e198-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="4e198-122">Suspend</span></span>

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

### <span data-ttu-id="4e198-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4e198-123">-InformationVariable</span></span>
<span data-ttu-id="4e198-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="4e198-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4e198-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="4e198-125">-Profile</span></span>
<span data-ttu-id="4e198-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4e198-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4e198-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4e198-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4e198-128">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="4e198-128">-ServiceName</span></span>
<span data-ttu-id="4e198-129">Annak a szolgáltatásnak a nevét adja meg, amelynek a parancsmagja a termelést és az átmeneti telepítési példányokat felcseréli.</span><span class="sxs-lookup"><span data-stu-id="4e198-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="4e198-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e198-130">CommonParameters</span></span>
<span data-ttu-id="4e198-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e198-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e198-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e198-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e198-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e198-133">INPUTS</span></span>

## <span data-ttu-id="4e198-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e198-134">OUTPUTS</span></span>

### <span data-ttu-id="4e198-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4e198-135">ManagementOperationContext</span></span>

## <span data-ttu-id="4e198-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e198-136">NOTES</span></span>

## <span data-ttu-id="4e198-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e198-137">RELATED LINKS</span></span>

[<span data-ttu-id="4e198-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4e198-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="4e198-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="4e198-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="4e198-140">Új – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4e198-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="4e198-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4e198-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="4e198-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4e198-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


