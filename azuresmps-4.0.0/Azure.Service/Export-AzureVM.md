---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015677"
---
# <span data-ttu-id="a4035-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a4035-101">Export-AzureVM</span></span>

## <span data-ttu-id="a4035-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4035-102">SYNOPSIS</span></span>
<span data-ttu-id="a4035-103">Azure Virtual Machine-állam exportálása fájlba</span><span class="sxs-lookup"><span data-stu-id="a4035-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="a4035-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4035-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a4035-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4035-105">DESCRIPTION</span></span>
<span data-ttu-id="a4035-106">Az **export-AzureVM** parancsmag a virtuális gép állapotát. XML fájlba exportálja.</span><span class="sxs-lookup"><span data-stu-id="a4035-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="a4035-107">Az **AzureVM** futtatása után az **Eltávolítás – AzureVM** , majd az **Importálás – AzureVM** parancsra kattintva a virtuális gép újból létrehozhatja a virtuális gépet, mert az eredetitől eltérő IP-cím lehet.</span><span class="sxs-lookup"><span data-stu-id="a4035-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="a4035-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a4035-108">EXAMPLES</span></span>

### <span data-ttu-id="a4035-109">1. példa: virtuális gép exportálása</span><span class="sxs-lookup"><span data-stu-id="a4035-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="a4035-110">Ez a parancs a megadott virtuális gép állapotát a VMstate.xml fájlba exportálja.</span><span class="sxs-lookup"><span data-stu-id="a4035-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="a4035-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4035-111">PARAMETERS</span></span>

### <span data-ttu-id="a4035-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a4035-112">-InformationAction</span></span>
<span data-ttu-id="a4035-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="a4035-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a4035-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a4035-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4035-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="a4035-115">Continue</span></span>
- <span data-ttu-id="a4035-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="a4035-116">Ignore</span></span>
- <span data-ttu-id="a4035-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="a4035-117">Inquire</span></span>
- <span data-ttu-id="a4035-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a4035-118">SilentlyContinue</span></span>
- <span data-ttu-id="a4035-119">állj</span><span class="sxs-lookup"><span data-stu-id="a4035-119">Stop</span></span>
- <span data-ttu-id="a4035-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="a4035-120">Suspend</span></span>

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

### <span data-ttu-id="a4035-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a4035-121">-InformationVariable</span></span>
<span data-ttu-id="a4035-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a4035-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a4035-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4035-123">-Name</span></span>
<span data-ttu-id="a4035-124">Annak a virtuális gépnek a neve, amelyhez a parancsmag exportálja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="a4035-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4035-125">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a4035-125">-Path</span></span>
<span data-ttu-id="a4035-126">Annak az elérési útját és fájlnevet adja meg, amelyre a parancsmag a virtuális gép állapotát menti.</span><span class="sxs-lookup"><span data-stu-id="a4035-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4035-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="a4035-127">-Profile</span></span>
<span data-ttu-id="a4035-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a4035-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a4035-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a4035-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4035-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a4035-130">-ServiceName</span></span>
<span data-ttu-id="a4035-131">A virtuális gépet tároló Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4035-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="a4035-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4035-132">CommonParameters</span></span>
<span data-ttu-id="a4035-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4035-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4035-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4035-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4035-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4035-135">INPUTS</span></span>

## <span data-ttu-id="a4035-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4035-136">OUTPUTS</span></span>

## <span data-ttu-id="a4035-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4035-137">NOTES</span></span>

## <span data-ttu-id="a4035-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4035-138">RELATED LINKS</span></span>

[<span data-ttu-id="a4035-139">Importálás – AzureVM</span><span class="sxs-lookup"><span data-stu-id="a4035-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


