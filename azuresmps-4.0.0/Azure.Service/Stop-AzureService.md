---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015807"
---
# <span data-ttu-id="848f1-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="848f1-101">Stop-AzureService</span></span>

## <span data-ttu-id="848f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="848f1-102">SYNOPSIS</span></span>
<span data-ttu-id="848f1-103">Leállítja az aktuálisan hosztolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="848f1-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="848f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="848f1-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="848f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="848f1-105">DESCRIPTION</span></span>
<span data-ttu-id="848f1-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="848f1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="848f1-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="848f1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="848f1-108">A **stop-AzureService** parancsmag leállítja a Windows Azure által megadott bővítőhelyen a jelenlegi hosztolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="848f1-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="848f1-109">Ha nincs megadva bővítőhely, a parancsmag leállítja a szolgáltatást a termelési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="848f1-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="848f1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="848f1-110">EXAMPLES</span></span>

## <span data-ttu-id="848f1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="848f1-111">PARAMETERS</span></span>

### <span data-ttu-id="848f1-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="848f1-112">-PassThru</span></span>
<span data-ttu-id="848f1-113">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="848f1-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="848f1-114">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="848f1-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="848f1-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="848f1-115">-Profile</span></span>
<span data-ttu-id="848f1-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="848f1-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="848f1-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="848f1-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="848f1-118">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="848f1-118">-ServiceName</span></span>
<span data-ttu-id="848f1-119">A leállításhoz a hosztolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="848f1-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="848f1-120">Ha nincs megadva név, a parancsmag leállítja az aktuálisan hosztolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="848f1-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="848f1-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="848f1-121">-Slot</span></span>
<span data-ttu-id="848f1-122">Azt a bővítőhelyet adja meg, ahol a szolgáltatást üzemelteti, vagy az átmeneti vagy a gyártási időpontot.</span><span class="sxs-lookup"><span data-stu-id="848f1-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="848f1-123">Ha nincs megadva bővítőhely, a program a termelést veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="848f1-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="848f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848f1-124">CommonParameters</span></span>
<span data-ttu-id="848f1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="848f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848f1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="848f1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848f1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="848f1-127">INPUTS</span></span>

## <span data-ttu-id="848f1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="848f1-128">OUTPUTS</span></span>

## <span data-ttu-id="848f1-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="848f1-129">NOTES</span></span>

## <span data-ttu-id="848f1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="848f1-130">RELATED LINKS</span></span>

[<span data-ttu-id="848f1-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="848f1-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="848f1-132">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="848f1-132">Start-AzureService</span></span>](./Start-AzureService.md)


