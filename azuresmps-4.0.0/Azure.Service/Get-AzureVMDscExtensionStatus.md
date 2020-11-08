---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016536"
---
# <span data-ttu-id="b51a2-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="b51a2-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="b51a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b51a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b51a2-103">A DSC kiterjesztési állapotot kapja minden olyan virtuális gépen, amelyet a Felhőbeli szolgáltatásokban vagy a szolgáltatás adott virtuális gépén telepített.</span><span class="sxs-lookup"><span data-stu-id="b51a2-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="b51a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b51a2-104">SYNTAX</span></span>

### <span data-ttu-id="b51a2-105">GetStatusByServiceAndVMName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b51a2-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b51a2-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="b51a2-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b51a2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b51a2-107">DESCRIPTION</span></span>
<span data-ttu-id="b51a2-108">A **Get-AzureVMDscExtensionStatus** parancsmag a megfelelő állapot-beállítási (DSC) kiterjesztési állapotot kapja meg a felhőalapú szolgáltatásban vagy a szolgáltatás adott virtuális gépén telepített összes virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="b51a2-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="b51a2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b51a2-109">EXAMPLES</span></span>

### <span data-ttu-id="b51a2-110">1:</span><span class="sxs-lookup"><span data-stu-id="b51a2-110">1:</span></span>
```

```

## <span data-ttu-id="b51a2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b51a2-111">PARAMETERS</span></span>

### <span data-ttu-id="b51a2-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b51a2-112">-InformationAction</span></span>
<span data-ttu-id="b51a2-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b51a2-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b51a2-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b51a2-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b51a2-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b51a2-115">Continue</span></span>
- <span data-ttu-id="b51a2-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b51a2-116">Ignore</span></span>
- <span data-ttu-id="b51a2-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b51a2-117">Inquire</span></span>
- <span data-ttu-id="b51a2-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b51a2-118">SilentlyContinue</span></span>
- <span data-ttu-id="b51a2-119">állj</span><span class="sxs-lookup"><span data-stu-id="b51a2-119">Stop</span></span>
- <span data-ttu-id="b51a2-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b51a2-120">Suspend</span></span>

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

### <span data-ttu-id="b51a2-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b51a2-121">-InformationVariable</span></span>
<span data-ttu-id="b51a2-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b51a2-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b51a2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b51a2-123">-Name</span></span>
<span data-ttu-id="b51a2-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51a2-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51a2-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="b51a2-125">-Profile</span></span>
<span data-ttu-id="b51a2-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b51a2-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b51a2-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b51a2-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b51a2-128">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="b51a2-128">-ServiceName</span></span>
<span data-ttu-id="b51a2-129">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51a2-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51a2-130">-VM</span><span class="sxs-lookup"><span data-stu-id="b51a2-130">-VM</span></span>
<span data-ttu-id="b51a2-131">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51a2-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b51a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51a2-132">CommonParameters</span></span>
<span data-ttu-id="b51a2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b51a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51a2-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b51a2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51a2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b51a2-135">INPUTS</span></span>

## <span data-ttu-id="b51a2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b51a2-136">OUTPUTS</span></span>

### <span data-ttu-id="b51a2-137">Microsoft. WindowsAzure. Command. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="b51a2-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="b51a2-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b51a2-138">NOTES</span></span>

## <span data-ttu-id="b51a2-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b51a2-139">RELATED LINKS</span></span>

[<span data-ttu-id="b51a2-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b51a2-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="b51a2-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b51a2-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="b51a2-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b51a2-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


