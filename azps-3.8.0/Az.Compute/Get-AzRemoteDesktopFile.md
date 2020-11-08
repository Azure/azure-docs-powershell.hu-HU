---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 650602ef229dd6c7371c6befebbb15dacae1d706
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013432"
---
# <span data-ttu-id="e1e1f-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="e1e1f-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="e1e1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e1f-103">. Rdp fájlok beolvasása</span><span class="sxs-lookup"><span data-stu-id="e1e1f-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="e1e1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1e1f-104">SYNTAX</span></span>

### <span data-ttu-id="e1e1f-105">Letöltés</span><span class="sxs-lookup"><span data-stu-id="e1e1f-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e1f-106">Rovatok sávon</span><span class="sxs-lookup"><span data-stu-id="e1e1f-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1e1f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1e1f-107">DESCRIPTION</span></span>
<span data-ttu-id="e1e1f-108">A **Get-AzRemoteDesktopFile** parancsmag egy Remote Desktop Protocol (. rdp) fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="e1e1f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e1e1f-109">EXAMPLES</span></span>

### <span data-ttu-id="e1e1f-110">Példa 1: távoli asztali fájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="e1e1f-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="e1e1f-111">Ez a parancs a VirtualMachine07 nevű virtuális gép távoli asztali fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="e1e1f-112">A parancs az eredményt a D:\RemoteDesktopFile07.rdp. nevű fájlban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="e1e1f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1e1f-113">PARAMETERS</span></span>

### <span data-ttu-id="e1e1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e1f-114">-DefaultProfile</span></span>
<span data-ttu-id="e1e1f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1e1f-116">-Launch (indítás)</span><span class="sxs-lookup"><span data-stu-id="e1e1f-116">-Launch</span></span>
<span data-ttu-id="e1e1f-117">Azt jelzi, hogy ez a parancsmag elindítja a Távoli asztalt, miután az. rdp-fájlt bekapja.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="e1e1f-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="e1e1f-118">-LocalPath</span></span>
<span data-ttu-id="e1e1f-119">Annak a helyi teljes elérési útját adja meg, ahol a parancsmag az. rdp fájlt tárolja.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="e1e1f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1e1f-120">-Name</span></span>
<span data-ttu-id="e1e1f-121">Annak az elérhetőségi készletnek a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e1e1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1e1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1e1f-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e1e1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e1f-124">CommonParameters</span></span>
<span data-ttu-id="e1e1f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1e1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e1f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1e1f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e1f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1e1f-127">INPUTS</span></span>

### <span data-ttu-id="e1e1f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e1e1f-128">System.String</span></span>

## <span data-ttu-id="e1e1f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1e1f-129">OUTPUTS</span></span>

### <span data-ttu-id="e1e1f-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="e1e1f-130">System.Void</span></span>

## <span data-ttu-id="e1e1f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1e1f-131">NOTES</span></span>

## <span data-ttu-id="e1e1f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1e1f-132">RELATED LINKS</span></span>
