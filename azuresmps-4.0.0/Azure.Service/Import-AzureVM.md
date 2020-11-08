---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016255"
---
# <span data-ttu-id="b7078-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b7078-101">Import-AzureVM</span></span>

## <span data-ttu-id="b7078-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7078-102">SYNOPSIS</span></span>
<span data-ttu-id="b7078-103">Azure Virtual Machine-állam importálása fájlból.</span><span class="sxs-lookup"><span data-stu-id="b7078-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="b7078-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7078-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7078-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7078-105">DESCRIPTION</span></span>
<span data-ttu-id="b7078-106">Az **import-AzureVM** parancsmag a virtuális gép korábban mentett állapotát XML-fájlból importálja.</span><span class="sxs-lookup"><span data-stu-id="b7078-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="b7078-107">Ez a parancsmag akkor hasznos, ha később egy virtuális gépet szeretne létrehozni az importált adatforrásból.</span><span class="sxs-lookup"><span data-stu-id="b7078-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="b7078-108">Az **AzureVM** futtatása után az **Eltávolítás – AzureVM** , majd az **Importálás – AzureVM** parancsra kattintva a virtuális gép újból létrehozhatja a virtuális gépet, mert az eredetitől eltérő IP-cím lehet.</span><span class="sxs-lookup"><span data-stu-id="b7078-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="b7078-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b7078-109">EXAMPLES</span></span>

### <span data-ttu-id="b7078-110">1. példa: virtuálisgép-állapot importálása</span><span class="sxs-lookup"><span data-stu-id="b7078-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="b7078-111">Ezzel a paranccsal importálhatja egy virtuális gép állapotát a VMstate.xml-fájlból, majd egy virtuális gépet hoz létre a megadott Felhőbeli szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b7078-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="b7078-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7078-112">PARAMETERS</span></span>

### <span data-ttu-id="b7078-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b7078-113">-InformationAction</span></span>
<span data-ttu-id="b7078-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b7078-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b7078-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b7078-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7078-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b7078-116">Continue</span></span>
- <span data-ttu-id="b7078-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b7078-117">Ignore</span></span>
- <span data-ttu-id="b7078-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b7078-118">Inquire</span></span>
- <span data-ttu-id="b7078-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b7078-119">SilentlyContinue</span></span>
- <span data-ttu-id="b7078-120">állj</span><span class="sxs-lookup"><span data-stu-id="b7078-120">Stop</span></span>
- <span data-ttu-id="b7078-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b7078-121">Suspend</span></span>

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

### <span data-ttu-id="b7078-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b7078-122">-InformationVariable</span></span>
<span data-ttu-id="b7078-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b7078-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b7078-124">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b7078-124">-Path</span></span>
<span data-ttu-id="b7078-125">A korábban mentett virtuálisgép-állapottal rendelkező fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7078-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

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

### <span data-ttu-id="b7078-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7078-126">CommonParameters</span></span>
<span data-ttu-id="b7078-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7078-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7078-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7078-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7078-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7078-129">INPUTS</span></span>

## <span data-ttu-id="b7078-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7078-130">OUTPUTS</span></span>

## <span data-ttu-id="b7078-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7078-131">NOTES</span></span>

## <span data-ttu-id="b7078-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7078-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7078-133">Exportálás – AzureVM</span><span class="sxs-lookup"><span data-stu-id="b7078-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="b7078-134">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="b7078-134">New-AzureVM</span></span>](./New-AzureVM.md)


