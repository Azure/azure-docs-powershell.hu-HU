---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016031"
---
# <span data-ttu-id="8944c-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="8944c-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="8944c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8944c-102">SYNOPSIS</span></span>
<span data-ttu-id="8944c-103">Elindítja a számítási és a tárolási emulátort.</span><span class="sxs-lookup"><span data-stu-id="8944c-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="8944c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8944c-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8944c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8944c-105">DESCRIPTION</span></span>
<span data-ttu-id="8944c-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="8944c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8944c-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8944c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8944c-108">A **Start-AzureEmulator** parancsmag mind a számítási, mind a tároló emulátorral elindul, és az aktuális szolgáltatást a számítási emulátorban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8944c-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="8944c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8944c-109">EXAMPLES</span></span>

### <span data-ttu-id="8944c-110">1. példa: az emulátor elindítása és a böngésző elindítása</span><span class="sxs-lookup"><span data-stu-id="8944c-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="8944c-111">Ez a példa futtatja a szolgáltatást az Azure emulátorban, és egy új böngészőablakot indít az emulált szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8944c-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="8944c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8944c-112">PARAMETERS</span></span>

### <span data-ttu-id="8944c-113">-Launch (indítás)</span><span class="sxs-lookup"><span data-stu-id="8944c-113">-Launch</span></span>
<span data-ttu-id="8944c-114">Az emulátorban való üzemeltetés után megnyílik egy új böngészőablak a szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8944c-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8944c-115">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="8944c-115">-Mode</span></span>
<span data-ttu-id="8944c-116">Az emulátor üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8944c-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="8944c-117">Az érvényes értékek: teljes és expressz.</span><span class="sxs-lookup"><span data-stu-id="8944c-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="8944c-118">Az alapértelmezett érték az Express.</span><span class="sxs-lookup"><span data-stu-id="8944c-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8944c-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="8944c-119">-Profile</span></span>
<span data-ttu-id="8944c-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8944c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8944c-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8944c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8944c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8944c-122">CommonParameters</span></span>
<span data-ttu-id="8944c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8944c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8944c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8944c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8944c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8944c-125">INPUTS</span></span>

## <span data-ttu-id="8944c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8944c-126">OUTPUTS</span></span>

## <span data-ttu-id="8944c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8944c-127">NOTES</span></span>

## <span data-ttu-id="8944c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8944c-128">RELATED LINKS</span></span>

[<span data-ttu-id="8944c-129">Új – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="8944c-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="8944c-130">Közzététel – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="8944c-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="8944c-131">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="8944c-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


