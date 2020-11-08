---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015645"
---
# <span data-ttu-id="50836-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="50836-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="50836-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50836-102">SYNOPSIS</span></span>
<span data-ttu-id="50836-103">Információt kap az Azure Virtual Machine rendszerhez rendelt végpontokról.</span><span class="sxs-lookup"><span data-stu-id="50836-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="50836-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50836-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="50836-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50836-105">DESCRIPTION</span></span>
<span data-ttu-id="50836-106">A **Get-AzureEndpoint** parancsmag információt kap az Azure Virtual Machine rendszerhez rendelt végpontokról.</span><span class="sxs-lookup"><span data-stu-id="50836-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="50836-107">Példák</span><span class="sxs-lookup"><span data-stu-id="50836-107">EXAMPLES</span></span>

### <span data-ttu-id="50836-108">Példa 1: a virtuális gép végpontjának adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="50836-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="50836-109">Ez a parancs a **Get-AzureVM** parancsmag használatával lekérdezi a VirtualMachine12 nevű virtuális gép konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="50836-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="50836-110">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="50836-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="50836-111">Ez a parancsmag a virtuális gép végpontjának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="50836-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="50836-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50836-112">PARAMETERS</span></span>

### <span data-ttu-id="50836-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="50836-113">-InformationAction</span></span>
<span data-ttu-id="50836-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="50836-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="50836-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="50836-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50836-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="50836-116">Continue</span></span>
- <span data-ttu-id="50836-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="50836-117">Ignore</span></span>
- <span data-ttu-id="50836-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="50836-118">Inquire</span></span>
- <span data-ttu-id="50836-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="50836-119">SilentlyContinue</span></span>
- <span data-ttu-id="50836-120">állj</span><span class="sxs-lookup"><span data-stu-id="50836-120">Stop</span></span>
- <span data-ttu-id="50836-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="50836-121">Suspend</span></span>

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

### <span data-ttu-id="50836-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="50836-122">-InformationVariable</span></span>
<span data-ttu-id="50836-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="50836-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="50836-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50836-124">-Name</span></span>
<span data-ttu-id="50836-125">Annak a végpontnak a nevét adja meg, amelyhez ez a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="50836-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50836-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="50836-126">-Profile</span></span>
<span data-ttu-id="50836-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="50836-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50836-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="50836-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50836-129">-VM</span><span class="sxs-lookup"><span data-stu-id="50836-129">-VM</span></span>
<span data-ttu-id="50836-130">Azt a virtuális gépet adja meg, amelyből a parancsmag végpont-információt kap.</span><span class="sxs-lookup"><span data-stu-id="50836-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

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

### <span data-ttu-id="50836-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50836-131">CommonParameters</span></span>
<span data-ttu-id="50836-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50836-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50836-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50836-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50836-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50836-134">INPUTS</span></span>

## <span data-ttu-id="50836-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50836-135">OUTPUTS</span></span>

## <span data-ttu-id="50836-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50836-136">NOTES</span></span>

## <span data-ttu-id="50836-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50836-137">RELATED LINKS</span></span>

[<span data-ttu-id="50836-138">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="50836-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="50836-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="50836-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="50836-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="50836-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="50836-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="50836-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


