---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016332"
---
# <span data-ttu-id="61b5f-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="61b5f-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="61b5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="61b5f-103">Az Azure Virtual Machine operációs rendszer lemezének beolvasása.</span><span class="sxs-lookup"><span data-stu-id="61b5f-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="61b5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61b5f-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="61b5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="61b5f-106">A **Get-AzureOSDisk** parancsmag az Azure Virtual Machine operációs rendszer lemezét kapja.</span><span class="sxs-lookup"><span data-stu-id="61b5f-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="61b5f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="61b5f-107">EXAMPLES</span></span>

### <span data-ttu-id="61b5f-108">1. példa: operációs rendszer lemezének beszerzése</span><span class="sxs-lookup"><span data-stu-id="61b5f-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="61b5f-109">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine02 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="61b5f-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="61b5f-110">A parancs a virtuális gépet az aktuális parancsmagba továbbítja a csővezeték-kezelő segítségével.</span><span class="sxs-lookup"><span data-stu-id="61b5f-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61b5f-111">Az aktuális parancsmag a virtuális gép operációs rendszerének lemezét kapja.</span><span class="sxs-lookup"><span data-stu-id="61b5f-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="61b5f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61b5f-112">PARAMETERS</span></span>

### <span data-ttu-id="61b5f-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="61b5f-113">-InformationAction</span></span>
<span data-ttu-id="61b5f-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="61b5f-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="61b5f-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="61b5f-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61b5f-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="61b5f-116">Continue</span></span>
- <span data-ttu-id="61b5f-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="61b5f-117">Ignore</span></span>
- <span data-ttu-id="61b5f-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="61b5f-118">Inquire</span></span>
- <span data-ttu-id="61b5f-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="61b5f-119">SilentlyContinue</span></span>
- <span data-ttu-id="61b5f-120">állj</span><span class="sxs-lookup"><span data-stu-id="61b5f-120">Stop</span></span>
- <span data-ttu-id="61b5f-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="61b5f-121">Suspend</span></span>

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

### <span data-ttu-id="61b5f-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="61b5f-122">-InformationVariable</span></span>
<span data-ttu-id="61b5f-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="61b5f-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="61b5f-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="61b5f-124">-Profile</span></span>
<span data-ttu-id="61b5f-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="61b5f-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61b5f-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="61b5f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61b5f-127">-VM</span><span class="sxs-lookup"><span data-stu-id="61b5f-127">-VM</span></span>
<span data-ttu-id="61b5f-128">Azt a virtuális gépet adja meg, amelyhez ez a parancsmag az operációs rendszer lemezét kapja.</span><span class="sxs-lookup"><span data-stu-id="61b5f-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="61b5f-129">Virtuális gép objektum beszerzéséhez használja a **Get-AzureVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="61b5f-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="61b5f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b5f-130">CommonParameters</span></span>
<span data-ttu-id="61b5f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61b5f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b5f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b5f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b5f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61b5f-133">INPUTS</span></span>

## <span data-ttu-id="61b5f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61b5f-134">OUTPUTS</span></span>

## <span data-ttu-id="61b5f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61b5f-135">NOTES</span></span>

## <span data-ttu-id="61b5f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61b5f-136">RELATED LINKS</span></span>

[<span data-ttu-id="61b5f-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="61b5f-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="61b5f-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="61b5f-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


