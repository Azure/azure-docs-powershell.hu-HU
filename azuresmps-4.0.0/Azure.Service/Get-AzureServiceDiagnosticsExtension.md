---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015603"
---
# <span data-ttu-id="5ceae-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5ceae-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="5ceae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ceae-102">SYNOPSIS</span></span>
<span data-ttu-id="5ceae-103">A felhőalapú szolgáltatás diagnosztikai bővítményének beírása az összes szerepkörben vagy az elnevezett szerepkörökben egy bizonyos terjesztési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="5ceae-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="5ceae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ceae-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ceae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ceae-105">DESCRIPTION</span></span>
<span data-ttu-id="5ceae-106">A **Get-AzureServiceDiagnosticsExtension** parancsmag a felhőalapú szolgáltatás diagnosztikai bővítményét alkalmazza az összes szerepkörben vagy elnevezett szerepkörökben egy bizonyos terjesztési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="5ceae-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="5ceae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5ceae-107">EXAMPLES</span></span>

### <span data-ttu-id="5ceae-108">1. példa: a szolgáltatás-diagnosztika bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="5ceae-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="5ceae-109">Ez a parancs minden szerepkörben megkapja a szolgáltatás diagnosztikai szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="5ceae-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="5ceae-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ceae-110">PARAMETERS</span></span>

### <span data-ttu-id="5ceae-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5ceae-111">-InformationAction</span></span>
<span data-ttu-id="5ceae-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5ceae-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5ceae-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5ceae-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ceae-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5ceae-114">Continue</span></span>
- <span data-ttu-id="5ceae-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5ceae-115">Ignore</span></span>
- <span data-ttu-id="5ceae-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5ceae-116">Inquire</span></span>
- <span data-ttu-id="5ceae-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5ceae-117">SilentlyContinue</span></span>
- <span data-ttu-id="5ceae-118">állj</span><span class="sxs-lookup"><span data-stu-id="5ceae-118">Stop</span></span>
- <span data-ttu-id="5ceae-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5ceae-119">Suspend</span></span>

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

### <span data-ttu-id="5ceae-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5ceae-120">-InformationVariable</span></span>
<span data-ttu-id="5ceae-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5ceae-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5ceae-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ceae-122">-Profile</span></span>
<span data-ttu-id="5ceae-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5ceae-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ceae-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5ceae-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ceae-125">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="5ceae-125">-Role</span></span>
<span data-ttu-id="5ceae-126">A szerepkörök tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ceae-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ceae-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="5ceae-127">-ServiceName</span></span>
<span data-ttu-id="5ceae-128">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ceae-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="5ceae-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="5ceae-129">-Slot</span></span>
<span data-ttu-id="5ceae-130">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ceae-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="5ceae-131">A paraméter elfogadható értékei a következők: termelés vagy megállóhely.</span><span class="sxs-lookup"><span data-stu-id="5ceae-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="5ceae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ceae-132">CommonParameters</span></span>
<span data-ttu-id="5ceae-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ceae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ceae-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ceae-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ceae-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ceae-135">INPUTS</span></span>

## <span data-ttu-id="5ceae-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ceae-136">OUTPUTS</span></span>

## <span data-ttu-id="5ceae-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ceae-137">NOTES</span></span>

## <span data-ttu-id="5ceae-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ceae-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ceae-139">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5ceae-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="5ceae-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5ceae-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


