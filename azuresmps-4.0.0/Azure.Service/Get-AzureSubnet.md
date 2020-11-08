---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015543"
---
# <span data-ttu-id="f61e1-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="f61e1-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="f61e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f61e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f61e1-103">A megadott Azure virtuális géphez társított alhálózatok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="f61e1-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="f61e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f61e1-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f61e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f61e1-105">DESCRIPTION</span></span>
<span data-ttu-id="f61e1-106">A **Get-AzureSubnet** parancsmag egy olyan listát ad eredményül, amely a megadott virtuális géphez társított alhálózatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f61e1-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="f61e1-107">Használja a **Get-AzureVM** a virtuális gép megadásához.</span><span class="sxs-lookup"><span data-stu-id="f61e1-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="f61e1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f61e1-108">EXAMPLES</span></span>

### <span data-ttu-id="f61e1-109">1. példa: alhálózatok beszerzése virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="f61e1-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="f61e1-110">Az első parancs a VirtualMachine01 nevű virtuális gépet kapja a ContosoService03 nevű szolgáltatásban, majd a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f61e1-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="f61e1-111">A második parancs beolvassa a virtuális gép Azure alhálózatait a $VMban.</span><span class="sxs-lookup"><span data-stu-id="f61e1-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="f61e1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f61e1-112">PARAMETERS</span></span>

### <span data-ttu-id="f61e1-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f61e1-113">-InformationAction</span></span>
<span data-ttu-id="f61e1-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f61e1-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f61e1-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f61e1-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f61e1-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f61e1-116">Continue</span></span>
- <span data-ttu-id="f61e1-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f61e1-117">Ignore</span></span>
- <span data-ttu-id="f61e1-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f61e1-118">Inquire</span></span>
- <span data-ttu-id="f61e1-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f61e1-119">SilentlyContinue</span></span>
- <span data-ttu-id="f61e1-120">állj</span><span class="sxs-lookup"><span data-stu-id="f61e1-120">Stop</span></span>
- <span data-ttu-id="f61e1-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f61e1-121">Suspend</span></span>

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

### <span data-ttu-id="f61e1-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f61e1-122">-InformationVariable</span></span>
<span data-ttu-id="f61e1-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f61e1-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f61e1-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="f61e1-124">-Profile</span></span>
<span data-ttu-id="f61e1-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f61e1-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f61e1-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f61e1-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f61e1-127">-VM</span><span class="sxs-lookup"><span data-stu-id="f61e1-127">-VM</span></span>
<span data-ttu-id="f61e1-128">Annak a virtuális gépnek az objektumát adja meg, amelyből be szeretné szerezni az alhálózati listát.</span><span class="sxs-lookup"><span data-stu-id="f61e1-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

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

### <span data-ttu-id="f61e1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61e1-129">CommonParameters</span></span>
<span data-ttu-id="f61e1-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f61e1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61e1-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f61e1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61e1-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f61e1-132">INPUTS</span></span>

## <span data-ttu-id="f61e1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f61e1-133">OUTPUTS</span></span>

## <span data-ttu-id="f61e1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f61e1-134">NOTES</span></span>

## <span data-ttu-id="f61e1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f61e1-135">RELATED LINKS</span></span>

[<span data-ttu-id="f61e1-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f61e1-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f61e1-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="f61e1-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


