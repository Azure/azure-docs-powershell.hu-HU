---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016505"
---
# <span data-ttu-id="98182-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="98182-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="98182-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98182-102">SYNOPSIS</span></span>
<span data-ttu-id="98182-103">Megkapja az URI-t a WinRM HTTPS-figyelőhöz egy virtuális géphez vagy egy hosztolt szolgáltatásban lévő virtuális gépek listájával.</span><span class="sxs-lookup"><span data-stu-id="98182-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="98182-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98182-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="98182-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98182-105">DESCRIPTION</span></span>
<span data-ttu-id="98182-106">A **Get-AzureWinRMUri** parancsmag a Windows távfelügyelet (WinRM) https-figyelésének URI-jét egy virtuális gépre vagy egy hosztolt szolgáltatás virtuális gépei listájára kapja.</span><span class="sxs-lookup"><span data-stu-id="98182-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="98182-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98182-107">EXAMPLES</span></span>

### <span data-ttu-id="98182-108">Példa 1: a WinRM HTTPS-figyelő URI-ja beszerzése virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="98182-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="98182-109">Ez a parancs a WinRM HTTPS-figyelő UIR a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="98182-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="98182-110">2. példa: a WinRM HTTPS-figyelő URI-azonosítójának beszerzése egy adott szolgáltatás virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="98182-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="98182-111">Ez a parancs a WinRM HTTPS-figyelő UIR a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="98182-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="98182-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98182-112">PARAMETERS</span></span>

### <span data-ttu-id="98182-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="98182-113">-InformationAction</span></span>
<span data-ttu-id="98182-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="98182-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="98182-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="98182-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98182-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="98182-116">Continue</span></span>
- <span data-ttu-id="98182-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="98182-117">Ignore</span></span>
- <span data-ttu-id="98182-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="98182-118">Inquire</span></span>
- <span data-ttu-id="98182-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="98182-119">SilentlyContinue</span></span>
- <span data-ttu-id="98182-120">állj</span><span class="sxs-lookup"><span data-stu-id="98182-120">Stop</span></span>
- <span data-ttu-id="98182-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="98182-121">Suspend</span></span>

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

### <span data-ttu-id="98182-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="98182-122">-InformationVariable</span></span>
<span data-ttu-id="98182-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="98182-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="98182-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98182-124">-Name</span></span>
<span data-ttu-id="98182-125">Annak a virtuális gépnek a neve, amelyhez a WinRM-URI jön létre.</span><span class="sxs-lookup"><span data-stu-id="98182-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

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

### <span data-ttu-id="98182-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="98182-126">-Profile</span></span>
<span data-ttu-id="98182-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="98182-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98182-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="98182-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98182-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="98182-129">-ServiceName</span></span>
<span data-ttu-id="98182-130">Annak a Microsoft Azure-szolgáltatásnak a neve, amely a virtuális gépet tárolja.</span><span class="sxs-lookup"><span data-stu-id="98182-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="98182-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98182-131">CommonParameters</span></span>
<span data-ttu-id="98182-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98182-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98182-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98182-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98182-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98182-134">INPUTS</span></span>

## <span data-ttu-id="98182-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98182-135">OUTPUTS</span></span>

## <span data-ttu-id="98182-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98182-136">NOTES</span></span>

## <span data-ttu-id="98182-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98182-137">RELATED LINKS</span></span>

[<span data-ttu-id="98182-138">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="98182-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="98182-139">Új – AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="98182-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


