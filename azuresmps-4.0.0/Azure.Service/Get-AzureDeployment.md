---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016355"
---
# <span data-ttu-id="3047e-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3047e-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="3047e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3047e-102">SYNOPSIS</span></span>
<span data-ttu-id="3047e-103">Beolvassa a telepített példány adatait.</span><span class="sxs-lookup"><span data-stu-id="3047e-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="3047e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3047e-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3047e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3047e-105">DESCRIPTION</span></span>
<span data-ttu-id="3047e-106">A **Get-AzureDeployment** parancsmag az Azure-alapú központi telepítését részletezi.</span><span class="sxs-lookup"><span data-stu-id="3047e-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="3047e-107">Adja meg az Azure-szolgáltatás nevét és a központi telepítő tárolóhelyét.</span><span class="sxs-lookup"><span data-stu-id="3047e-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="3047e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3047e-108">EXAMPLES</span></span>

### <span data-ttu-id="3047e-109">1. példa: a gyártási példány részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="3047e-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="3047e-110">Ez a parancs a ContosoService nevű szolgáltatás üzembe helyezésének részleteit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3047e-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="3047e-111">Ez a parancs nem ad meg tárolóhelyet.</span><span class="sxs-lookup"><span data-stu-id="3047e-111">This command does not specify a slot.</span></span>
<span data-ttu-id="3047e-112">Ezért a parancs a termelés alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="3047e-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="3047e-113">2. példa: a bevezetési beállítások részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="3047e-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="3047e-114">Ez a parancs a ContosoService bevezetési példányának részleteit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3047e-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="3047e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3047e-115">PARAMETERS</span></span>

### <span data-ttu-id="3047e-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3047e-116">-InformationAction</span></span>
<span data-ttu-id="3047e-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3047e-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3047e-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3047e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3047e-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3047e-119">Continue</span></span>
- <span data-ttu-id="3047e-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3047e-120">Ignore</span></span>
- <span data-ttu-id="3047e-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3047e-121">Inquire</span></span>
- <span data-ttu-id="3047e-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3047e-122">SilentlyContinue</span></span>
- <span data-ttu-id="3047e-123">állj</span><span class="sxs-lookup"><span data-stu-id="3047e-123">Stop</span></span>
- <span data-ttu-id="3047e-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3047e-124">Suspend</span></span>

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

### <span data-ttu-id="3047e-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3047e-125">-InformationVariable</span></span>
<span data-ttu-id="3047e-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3047e-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3047e-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="3047e-127">-Profile</span></span>
<span data-ttu-id="3047e-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3047e-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3047e-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3047e-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3047e-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="3047e-130">-ServiceName</span></span>
<span data-ttu-id="3047e-131">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3047e-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="3047e-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="3047e-132">-Slot</span></span>
<span data-ttu-id="3047e-133">A központi telepítő környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3047e-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="3047e-134">Érvényes értékek: staging vagy termelés.</span><span class="sxs-lookup"><span data-stu-id="3047e-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="3047e-135">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="3047e-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3047e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3047e-136">CommonParameters</span></span>
<span data-ttu-id="3047e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3047e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3047e-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3047e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3047e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3047e-139">INPUTS</span></span>

## <span data-ttu-id="3047e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3047e-140">OUTPUTS</span></span>

## <span data-ttu-id="3047e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3047e-141">NOTES</span></span>

## <span data-ttu-id="3047e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3047e-142">RELATED LINKS</span></span>

[<span data-ttu-id="3047e-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="3047e-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="3047e-144">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3047e-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="3047e-145">Új – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3047e-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="3047e-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3047e-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="3047e-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3047e-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


