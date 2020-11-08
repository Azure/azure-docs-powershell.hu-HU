---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016127"
---
# <span data-ttu-id="93bb7-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="93bb7-101">Remove-AzureService</span></span>

## <span data-ttu-id="93bb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="93bb7-103">Eltávolítja az aktuális felhő-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="93bb7-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="93bb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93bb7-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93bb7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="93bb7-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="93bb7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="93bb7-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="93bb7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="93bb7-108">A **Remove-AzureService** parancsmag leállítja és eltávolítja az aktuális Felhőbeli szolgáltatást, illetve a megadott szolgáltatáshoz és előfizetéshez tartozó szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="93bb7-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="93bb7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="93bb7-109">EXAMPLES</span></span>

## <span data-ttu-id="93bb7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93bb7-110">PARAMETERS</span></span>

### <span data-ttu-id="93bb7-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="93bb7-111">-DeleteAll</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="93bb7-112">-Force</span></span>
<span data-ttu-id="93bb7-113">A szolgáltatás eltávolítása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="93bb7-113">Removes the service without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb7-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93bb7-114">-PassThru</span></span>
<span data-ttu-id="93bb7-115">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="93bb7-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93bb7-116">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="93bb7-116">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="93bb7-117">-Profile</span></span>
<span data-ttu-id="93bb7-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="93bb7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93bb7-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="93bb7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93bb7-120">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="93bb7-120">-ServiceName</span></span>
<span data-ttu-id="93bb7-121">Az eltávolítani kívánt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93bb7-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="93bb7-122">Ha a parancsot egy szolgáltatási címtárból futtatja, és a név nincs megadva, akkor az aktuális szolgáltatás nevét használja.</span><span class="sxs-lookup"><span data-stu-id="93bb7-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93bb7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93bb7-123">-Confirm</span></span>
<span data-ttu-id="93bb7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93bb7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93bb7-125">-WhatIf</span></span>
<span data-ttu-id="93bb7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93bb7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93bb7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93bb7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bb7-128">CommonParameters</span></span>
<span data-ttu-id="93bb7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93bb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bb7-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93bb7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bb7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93bb7-131">INPUTS</span></span>

## <span data-ttu-id="93bb7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93bb7-132">OUTPUTS</span></span>

## <span data-ttu-id="93bb7-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93bb7-133">NOTES</span></span>

## <span data-ttu-id="93bb7-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93bb7-134">RELATED LINKS</span></span>

[<span data-ttu-id="93bb7-135">Közzététel – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="93bb7-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="93bb7-136">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="93bb7-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="93bb7-137">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="93bb7-137">Start-AzureService</span></span>](./Start-AzureService.md)


