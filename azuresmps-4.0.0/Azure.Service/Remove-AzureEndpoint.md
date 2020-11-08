---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016478"
---
# <span data-ttu-id="3c269-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c269-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="3c269-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c269-102">SYNOPSIS</span></span>
<span data-ttu-id="3c269-103">Egy Azure virtuális gépet futtató végpont törlése</span><span class="sxs-lookup"><span data-stu-id="3c269-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="3c269-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c269-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c269-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c269-105">DESCRIPTION</span></span>
<span data-ttu-id="3c269-106">A **Remove-AzureEndpoint** parancsmag az Azure Virtual Machine objektumból törli a végpontot.</span><span class="sxs-lookup"><span data-stu-id="3c269-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="3c269-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c269-107">EXAMPLES</span></span>

### <span data-ttu-id="3c269-108">1. példa: végpont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3c269-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="3c269-109">Ez a parancs a **Get-AzureVM** parancsmag használatával lekérdezi a VirtualMachine01 nevű virtuális gép konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3c269-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="3c269-110">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3c269-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3c269-111">Ez a parancsmag eltávolítja a HttpIn nevű végpontot.</span><span class="sxs-lookup"><span data-stu-id="3c269-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="3c269-112">A parancs átadja a virtuális gép objektumát a **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="3c269-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="3c269-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c269-113">PARAMETERS</span></span>

### <span data-ttu-id="3c269-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3c269-114">-InformationAction</span></span>
<span data-ttu-id="3c269-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3c269-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c269-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3c269-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c269-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3c269-117">Continue</span></span>
- <span data-ttu-id="3c269-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3c269-118">Ignore</span></span>
- <span data-ttu-id="3c269-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3c269-119">Inquire</span></span>
- <span data-ttu-id="3c269-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c269-120">SilentlyContinue</span></span>
- <span data-ttu-id="3c269-121">állj</span><span class="sxs-lookup"><span data-stu-id="3c269-121">Stop</span></span>
- <span data-ttu-id="3c269-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3c269-122">Suspend</span></span>

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

### <span data-ttu-id="3c269-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c269-123">-InformationVariable</span></span>
<span data-ttu-id="3c269-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3c269-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3c269-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c269-125">-Name</span></span>
<span data-ttu-id="3c269-126">Annak a végpontnak a nevét adja meg, amelynek a parancsmagja törlődik a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3c269-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c269-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c269-127">-Profile</span></span>
<span data-ttu-id="3c269-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3c269-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c269-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3c269-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c269-130">-VM</span><span class="sxs-lookup"><span data-stu-id="3c269-130">-VM</span></span>
<span data-ttu-id="3c269-131">Azt a virtuális gépet adja meg, amelyből ez a parancsmag töröl egy végpontot.</span><span class="sxs-lookup"><span data-stu-id="3c269-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="3c269-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c269-132">CommonParameters</span></span>
<span data-ttu-id="3c269-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c269-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c269-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c269-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c269-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c269-135">INPUTS</span></span>

## <span data-ttu-id="3c269-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c269-136">OUTPUTS</span></span>

## <span data-ttu-id="3c269-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c269-137">NOTES</span></span>

## <span data-ttu-id="3c269-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c269-138">RELATED LINKS</span></span>

[<span data-ttu-id="3c269-139">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c269-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="3c269-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c269-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="3c269-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3c269-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="3c269-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c269-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="3c269-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3c269-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


