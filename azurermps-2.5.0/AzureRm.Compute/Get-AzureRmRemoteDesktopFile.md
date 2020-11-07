---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
ms.openlocfilehash: e8b19272ed7b6c68221e34cef0395f0592b3013d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848925"
---
# <span data-ttu-id="d2649-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="d2649-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="d2649-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2649-102">SYNOPSIS</span></span>
<span data-ttu-id="d2649-103">. Rdp fájlok beolvasása</span><span class="sxs-lookup"><span data-stu-id="d2649-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2649-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2649-104">SYNTAX</span></span>

### <span data-ttu-id="d2649-105">Letöltés</span><span class="sxs-lookup"><span data-stu-id="d2649-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2649-106">Rovatok sávon</span><span class="sxs-lookup"><span data-stu-id="d2649-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2649-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2649-107">DESCRIPTION</span></span>
<span data-ttu-id="d2649-108">A **Get-AzureRmRemoteDesktopFile** parancsmag egy Remote Desktop Protocol (. rdp) fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="d2649-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="d2649-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d2649-109">EXAMPLES</span></span>

### <span data-ttu-id="d2649-110">Példa 1: távoli asztali fájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2649-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="d2649-111">Ez a parancs a VirtualMachine07 nevű virtuális gép távoli asztali fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2649-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="d2649-112">A parancs az eredményt a D:\RemoteDesktopFile07.rdp. nevű fájlban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d2649-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="d2649-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2649-113">PARAMETERS</span></span>

### <span data-ttu-id="d2649-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2649-114">-DefaultProfile</span></span>
<span data-ttu-id="d2649-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2649-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2649-116">-Launch (indítás)</span><span class="sxs-lookup"><span data-stu-id="d2649-116">-Launch</span></span>
<span data-ttu-id="d2649-117">Azt jelzi, hogy ez a parancsmag elindítja a Távoli asztalt, miután az. rdp-fájlt bekapja.</span><span class="sxs-lookup"><span data-stu-id="d2649-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2649-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="d2649-118">-LocalPath</span></span>
<span data-ttu-id="d2649-119">Annak a helyi teljes elérési útját adja meg, ahol a parancsmag az. rdp fájlt tárolja.</span><span class="sxs-lookup"><span data-stu-id="d2649-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2649-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2649-120">-Name</span></span>
<span data-ttu-id="d2649-121">Annak az elérhetőségi készletnek a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="d2649-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2649-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2649-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2649-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2649-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2649-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2649-124">CommonParameters</span></span>
<span data-ttu-id="d2649-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2649-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2649-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2649-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2649-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2649-127">INPUTS</span></span>

### <span data-ttu-id="d2649-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d2649-128">None</span></span>
<span data-ttu-id="d2649-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d2649-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2649-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2649-130">OUTPUTS</span></span>

## <span data-ttu-id="d2649-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2649-131">NOTES</span></span>

## <span data-ttu-id="d2649-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2649-132">RELATED LINKS</span></span>

