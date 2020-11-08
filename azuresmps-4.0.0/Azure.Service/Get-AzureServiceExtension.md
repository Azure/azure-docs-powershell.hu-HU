---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015599"
---
# <span data-ttu-id="117c5-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="117c5-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="117c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="117c5-102">SYNOPSIS</span></span>
<span data-ttu-id="117c5-103">A felhőben telepített bővítmények a telepített példányon.</span><span class="sxs-lookup"><span data-stu-id="117c5-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="117c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="117c5-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="117c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="117c5-105">DESCRIPTION</span></span>
<span data-ttu-id="117c5-106">A **Get-AzureServiceExtension** parancsmag a telepített Felhőbeli szolgáltatási bővítményeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="117c5-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="117c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="117c5-107">EXAMPLES</span></span>

### <span data-ttu-id="117c5-108">Példa 1: megadott bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="117c5-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="117c5-109">Ez a parancs a Felhőbeli szolgáltatások bővítményt a megadott névvel és névtérrel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="117c5-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="117c5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="117c5-110">PARAMETERS</span></span>

### <span data-ttu-id="117c5-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="117c5-111">-ExtensionName</span></span>
<span data-ttu-id="117c5-112">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117c5-112">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117c5-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="117c5-113">-InformationAction</span></span>
<span data-ttu-id="117c5-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="117c5-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="117c5-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="117c5-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="117c5-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="117c5-116">Continue</span></span>
- <span data-ttu-id="117c5-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="117c5-117">Ignore</span></span>
- <span data-ttu-id="117c5-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="117c5-118">Inquire</span></span>
- <span data-ttu-id="117c5-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="117c5-119">SilentlyContinue</span></span>
- <span data-ttu-id="117c5-120">állj</span><span class="sxs-lookup"><span data-stu-id="117c5-120">Stop</span></span>
- <span data-ttu-id="117c5-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="117c5-121">Suspend</span></span>

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

### <span data-ttu-id="117c5-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="117c5-122">-InformationVariable</span></span>
<span data-ttu-id="117c5-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="117c5-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="117c5-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="117c5-124">-Profile</span></span>
<span data-ttu-id="117c5-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="117c5-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="117c5-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="117c5-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="117c5-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="117c5-127">-ProviderNamespace</span></span>
<span data-ttu-id="117c5-128">A bővítmény-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117c5-128">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117c5-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="117c5-129">-ServiceName</span></span>
<span data-ttu-id="117c5-130">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117c5-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="117c5-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="117c5-131">-Slot</span></span>
<span data-ttu-id="117c5-132">A központi telepítő környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="117c5-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="117c5-133">A paraméter elfogadható értékei a következők: termelés vagy megállóhely.</span><span class="sxs-lookup"><span data-stu-id="117c5-133">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="117c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117c5-134">CommonParameters</span></span>
<span data-ttu-id="117c5-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="117c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117c5-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117c5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117c5-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="117c5-137">INPUTS</span></span>

## <span data-ttu-id="117c5-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="117c5-138">OUTPUTS</span></span>

## <span data-ttu-id="117c5-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="117c5-139">NOTES</span></span>

## <span data-ttu-id="117c5-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="117c5-140">RELATED LINKS</span></span>

[<span data-ttu-id="117c5-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="117c5-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="117c5-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="117c5-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


