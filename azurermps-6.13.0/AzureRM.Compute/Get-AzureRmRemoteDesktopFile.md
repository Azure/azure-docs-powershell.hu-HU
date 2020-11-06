---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: e6f3ba75247d8b5358e2a97c8bc635bbf805baec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494133"
---
# <span data-ttu-id="126f8-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="126f8-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="126f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="126f8-102">SYNOPSIS</span></span>
<span data-ttu-id="126f8-103">. Rdp fájlok beolvasása</span><span class="sxs-lookup"><span data-stu-id="126f8-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="126f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="126f8-104">SYNTAX</span></span>

### <span data-ttu-id="126f8-105">Letöltés</span><span class="sxs-lookup"><span data-stu-id="126f8-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="126f8-106">Rovatok sávon</span><span class="sxs-lookup"><span data-stu-id="126f8-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="126f8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="126f8-107">DESCRIPTION</span></span>
<span data-ttu-id="126f8-108">A **Get-AzureRmRemoteDesktopFile** parancsmag egy Remote Desktop Protocol (. rdp) fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="126f8-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="126f8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="126f8-109">EXAMPLES</span></span>

### <span data-ttu-id="126f8-110">Példa 1: távoli asztali fájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="126f8-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="126f8-111">Ez a parancs a VirtualMachine07 nevű virtuális gép távoli asztali fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="126f8-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="126f8-112">A parancs az eredményt a D:\RemoteDesktopFile07.rdp. nevű fájlban tárolja.</span><span class="sxs-lookup"><span data-stu-id="126f8-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="126f8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="126f8-113">PARAMETERS</span></span>

### <span data-ttu-id="126f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126f8-114">-DefaultProfile</span></span>
<span data-ttu-id="126f8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="126f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126f8-116">-Launch (indítás)</span><span class="sxs-lookup"><span data-stu-id="126f8-116">-Launch</span></span>
<span data-ttu-id="126f8-117">Azt jelzi, hogy ez a parancsmag elindítja a Távoli asztalt, miután az. rdp-fájlt bekapja.</span><span class="sxs-lookup"><span data-stu-id="126f8-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126f8-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="126f8-118">-LocalPath</span></span>
<span data-ttu-id="126f8-119">Annak a helyi teljes elérési útját adja meg, ahol a parancsmag az. rdp fájlt tárolja.</span><span class="sxs-lookup"><span data-stu-id="126f8-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126f8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="126f8-120">-Name</span></span>
<span data-ttu-id="126f8-121">Annak az elérhetőségi készletnek a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="126f8-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="126f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="126f8-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="126f8-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126f8-124">CommonParameters</span></span>
<span data-ttu-id="126f8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="126f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126f8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126f8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126f8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="126f8-127">INPUTS</span></span>

### <span data-ttu-id="126f8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="126f8-128">System.String</span></span>

## <span data-ttu-id="126f8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="126f8-129">OUTPUTS</span></span>

### <span data-ttu-id="126f8-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="126f8-130">System.Void</span></span>

## <span data-ttu-id="126f8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="126f8-131">NOTES</span></span>

## <span data-ttu-id="126f8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="126f8-132">RELATED LINKS</span></span>
