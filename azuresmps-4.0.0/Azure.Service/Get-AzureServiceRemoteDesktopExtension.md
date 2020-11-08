---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015596"
---
# <span data-ttu-id="64be7-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="64be7-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="64be7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64be7-102">SYNOPSIS</span></span>
<span data-ttu-id="64be7-103">Ez a parancsmag a felhőalapú szolgáltatás távoli asztali bővítményét alkalmazza az összes szerepkörben vagy elnevezett szerepkörökben egy bizonyos terjesztési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="64be7-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="64be7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64be7-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="64be7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64be7-105">DESCRIPTION</span></span>
<span data-ttu-id="64be7-106">A **Get-AzureServiceRemoteDesktopExtension** parancsmag a felhőalapú szolgáltatás távoli asztali bővítményét alkalmazza az összes szerepkörre vagy elnevezett szerepkörökre egy bizonyos terjesztési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="64be7-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="64be7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64be7-107">EXAMPLES</span></span>

### <span data-ttu-id="64be7-108">Példa 1: a távoli asztali bővítmény beszerzése a megadott szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="64be7-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="64be7-109">Ez a parancs a megadott szolgáltatáshoz tartozó távoli asztali bővítményt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="64be7-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="64be7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64be7-110">PARAMETERS</span></span>

### <span data-ttu-id="64be7-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="64be7-111">-InformationAction</span></span>
<span data-ttu-id="64be7-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="64be7-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="64be7-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="64be7-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64be7-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="64be7-114">Continue</span></span>
- <span data-ttu-id="64be7-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="64be7-115">Ignore</span></span>
- <span data-ttu-id="64be7-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="64be7-116">Inquire</span></span>
- <span data-ttu-id="64be7-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="64be7-117">SilentlyContinue</span></span>
- <span data-ttu-id="64be7-118">állj</span><span class="sxs-lookup"><span data-stu-id="64be7-118">Stop</span></span>
- <span data-ttu-id="64be7-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="64be7-119">Suspend</span></span>

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

### <span data-ttu-id="64be7-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="64be7-120">-InformationVariable</span></span>
<span data-ttu-id="64be7-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="64be7-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="64be7-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="64be7-122">-Profile</span></span>
<span data-ttu-id="64be7-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="64be7-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64be7-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="64be7-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64be7-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="64be7-125">-ServiceName</span></span>
<span data-ttu-id="64be7-126">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64be7-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64be7-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="64be7-127">-Slot</span></span>
<span data-ttu-id="64be7-128">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64be7-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="64be7-129">A paraméter elfogadható értékei a következők: termelés vagy megállóhely.</span><span class="sxs-lookup"><span data-stu-id="64be7-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64be7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64be7-130">CommonParameters</span></span>
<span data-ttu-id="64be7-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64be7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64be7-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64be7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64be7-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64be7-133">INPUTS</span></span>

## <span data-ttu-id="64be7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64be7-134">OUTPUTS</span></span>

## <span data-ttu-id="64be7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64be7-135">NOTES</span></span>

## <span data-ttu-id="64be7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64be7-136">RELATED LINKS</span></span>

[<span data-ttu-id="64be7-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="64be7-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


