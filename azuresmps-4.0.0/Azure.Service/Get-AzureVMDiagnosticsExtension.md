---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016543"
---
# <span data-ttu-id="5fb49-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5fb49-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="5fb49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fb49-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb49-103">Az Azure Diagnostics bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb49-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="5fb49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fb49-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5fb49-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fb49-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb49-106">A **Get-AzureVMDiagnosticsExtension** parancsmag a Microsoft Azure Diagnostics bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb49-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="5fb49-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5fb49-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb49-108">Példa 1: a diagnosztika bővítmény beszerzése virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="5fb49-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="5fb49-109">Ez a parancs a megadott virtuális gépre alkalmazott diagnosztikai bővítményt kapja meg a $VM változóban tárolt módon.</span><span class="sxs-lookup"><span data-stu-id="5fb49-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="5fb49-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fb49-110">PARAMETERS</span></span>

### <span data-ttu-id="5fb49-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5fb49-111">-InformationAction</span></span>
<span data-ttu-id="5fb49-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5fb49-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5fb49-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5fb49-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5fb49-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5fb49-114">Continue</span></span>
- <span data-ttu-id="5fb49-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5fb49-115">Ignore</span></span>
- <span data-ttu-id="5fb49-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5fb49-116">Inquire</span></span>
- <span data-ttu-id="5fb49-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5fb49-117">SilentlyContinue</span></span>
- <span data-ttu-id="5fb49-118">állj</span><span class="sxs-lookup"><span data-stu-id="5fb49-118">Stop</span></span>
- <span data-ttu-id="5fb49-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5fb49-119">Suspend</span></span>

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

### <span data-ttu-id="5fb49-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5fb49-120">-InformationVariable</span></span>
<span data-ttu-id="5fb49-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5fb49-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5fb49-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="5fb49-122">-Profile</span></span>
<span data-ttu-id="5fb49-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5fb49-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fb49-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5fb49-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fb49-125">-VM</span><span class="sxs-lookup"><span data-stu-id="5fb49-125">-VM</span></span>
<span data-ttu-id="5fb49-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb49-126">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb49-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb49-127">CommonParameters</span></span>
<span data-ttu-id="5fb49-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fb49-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb49-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb49-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb49-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb49-130">INPUTS</span></span>

## <span data-ttu-id="5fb49-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb49-131">OUTPUTS</span></span>

## <span data-ttu-id="5fb49-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fb49-132">NOTES</span></span>

## <span data-ttu-id="5fb49-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fb49-133">RELATED LINKS</span></span>

[<span data-ttu-id="5fb49-134">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5fb49-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="5fb49-135">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5fb49-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


