---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672757"
---
# <span data-ttu-id="1bd43-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="1bd43-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="1bd43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bd43-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd43-103">. Rdp fájlok beolvasása</span><span class="sxs-lookup"><span data-stu-id="1bd43-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bd43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bd43-104">SYNTAX</span></span>

### <span data-ttu-id="1bd43-105">Letöltés</span><span class="sxs-lookup"><span data-stu-id="1bd43-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="1bd43-106">Rovatok sávon</span><span class="sxs-lookup"><span data-stu-id="1bd43-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="1bd43-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bd43-107">DESCRIPTION</span></span>
<span data-ttu-id="1bd43-108">A **Get-AzureRmRemoteDesktopFile** parancsmag egy Remote Desktop Protocol (. rdp) fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="1bd43-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="1bd43-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1bd43-109">EXAMPLES</span></span>

### <span data-ttu-id="1bd43-110">Példa 1: távoli asztali fájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="1bd43-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="1bd43-111">Ez a parancs a VirtualMachine07 nevű virtuális gép távoli asztali fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1bd43-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="1bd43-112">A parancs az eredményt a D:\RemoteDesktopFile07.rdp. nevű fájlban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1bd43-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="1bd43-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bd43-113">PARAMETERS</span></span>

### <span data-ttu-id="1bd43-114">-Launch (indítás)</span><span class="sxs-lookup"><span data-stu-id="1bd43-114">-Launch</span></span>
<span data-ttu-id="1bd43-115">Azt jelzi, hogy ez a parancsmag elindítja a Távoli asztalt, miután az. rdp-fájlt bekapja.</span><span class="sxs-lookup"><span data-stu-id="1bd43-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="1bd43-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="1bd43-116">-LocalPath</span></span>
<span data-ttu-id="1bd43-117">Annak a helyi teljes elérési útját adja meg, ahol a parancsmag az. rdp fájlt tárolja.</span><span class="sxs-lookup"><span data-stu-id="1bd43-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="1bd43-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1bd43-118">-Name</span></span>
<span data-ttu-id="1bd43-119">Annak az elérhetőségi készletnek a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="1bd43-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1bd43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd43-120">-ResourceGroupName</span></span>
<span data-ttu-id="1bd43-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bd43-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1bd43-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd43-122">CommonParameters</span></span>
<span data-ttu-id="1bd43-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bd43-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd43-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd43-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd43-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bd43-125">INPUTS</span></span>

### <span data-ttu-id="1bd43-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="1bd43-126">None</span></span>
<span data-ttu-id="1bd43-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1bd43-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1bd43-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bd43-128">OUTPUTS</span></span>

## <span data-ttu-id="1bd43-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bd43-129">NOTES</span></span>

## <span data-ttu-id="1bd43-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bd43-130">RELATED LINKS</span></span>

