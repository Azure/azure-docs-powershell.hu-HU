---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015637"
---
# <span data-ttu-id="aa912-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="aa912-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="aa912-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa912-102">SYNOPSIS</span></span>
<span data-ttu-id="aa912-103">Felsorolja az összes Azure Guest operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="aa912-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="aa912-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa912-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aa912-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa912-105">DESCRIPTION</span></span>
<span data-ttu-id="aa912-106">A **Get-AzureOSVersion** parancsmag felsorolja az összes elérhető Azure Guest operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="aa912-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="aa912-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa912-107">EXAMPLES</span></span>

### <span data-ttu-id="aa912-108">Példa 1: az összes elérhető operációs rendszer beszerzése</span><span class="sxs-lookup"><span data-stu-id="aa912-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="aa912-109">Ez a parancs olyan objektumot olvas be, amely tartalmazza a vendég operációs rendszerek összes verziójának listáját a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="aa912-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="aa912-110">2. példa: az operációs rendszer adatainak megjelenítése táblázatban</span><span class="sxs-lookup"><span data-stu-id="aa912-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="aa912-111">Ez a parancs olyan objektumot olvas be, amely tartalmazza a vendég operációs rendszerek összes verziójának listáját a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="aa912-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="aa912-112">A parancs a pipeline operátor segítségével átadja őket a **Format-Table** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="aa912-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aa912-113">Az adott parancsmag olyan táblázatként formázza őket, amely az operációs rendszer családját, az operációs rendszer családi címkéjét és verzióját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="aa912-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="aa912-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa912-114">PARAMETERS</span></span>

### <span data-ttu-id="aa912-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aa912-115">-InformationAction</span></span>
<span data-ttu-id="aa912-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="aa912-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aa912-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aa912-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa912-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="aa912-118">Continue</span></span>
- <span data-ttu-id="aa912-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="aa912-119">Ignore</span></span>
- <span data-ttu-id="aa912-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="aa912-120">Inquire</span></span>
- <span data-ttu-id="aa912-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aa912-121">SilentlyContinue</span></span>
- <span data-ttu-id="aa912-122">állj</span><span class="sxs-lookup"><span data-stu-id="aa912-122">Stop</span></span>
- <span data-ttu-id="aa912-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="aa912-123">Suspend</span></span>

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

### <span data-ttu-id="aa912-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aa912-124">-InformationVariable</span></span>
<span data-ttu-id="aa912-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="aa912-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aa912-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="aa912-126">-Profile</span></span>
<span data-ttu-id="aa912-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="aa912-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa912-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="aa912-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa912-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa912-129">CommonParameters</span></span>
<span data-ttu-id="aa912-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa912-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa912-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa912-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa912-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa912-132">INPUTS</span></span>

## <span data-ttu-id="aa912-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa912-133">OUTPUTS</span></span>

## <span data-ttu-id="aa912-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa912-134">NOTES</span></span>

## <span data-ttu-id="aa912-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa912-135">RELATED LINKS</span></span>

[<span data-ttu-id="aa912-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="aa912-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


