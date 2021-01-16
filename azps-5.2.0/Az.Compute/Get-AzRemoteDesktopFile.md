---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 650602ef229dd6c7371c6befebbb15dacae1d706
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341213"
---
# <span data-ttu-id="4fe18-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="4fe18-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="4fe18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fe18-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe18-103">.rdp fájlt kap.</span><span class="sxs-lookup"><span data-stu-id="4fe18-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="4fe18-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4fe18-104">SYNTAX</span></span>

### <span data-ttu-id="4fe18-105">Letöltés</span><span class="sxs-lookup"><span data-stu-id="4fe18-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fe18-106">Indítás</span><span class="sxs-lookup"><span data-stu-id="4fe18-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fe18-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4fe18-107">DESCRIPTION</span></span>
<span data-ttu-id="4fe18-108">A **Get-AzRemoteDesktopFile** parancsmag távoli asztali protokollfájlt (.rdp) kap.</span><span class="sxs-lookup"><span data-stu-id="4fe18-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="4fe18-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4fe18-109">EXAMPLES</span></span>

### <span data-ttu-id="4fe18-110">1. példa: Távoli asztali fájl létrehozása</span><span class="sxs-lookup"><span data-stu-id="4fe18-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="4fe18-111">Ez a parancs a VirtualMachine07 nevű virtuális gép távoli asztalfájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4fe18-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="4fe18-112">A parancs a D:\RemoteDesktopFile07.rdp nevű fájlban tárolja az eredményt.</span><span class="sxs-lookup"><span data-stu-id="4fe18-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="4fe18-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fe18-113">PARAMETERS</span></span>

### <span data-ttu-id="4fe18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe18-114">-DefaultProfile</span></span>
<span data-ttu-id="4fe18-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fe18-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fe18-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="4fe18-116">-Launch</span></span>
<span data-ttu-id="4fe18-117">Azt jelzi, hogy ez a parancsmag elindítja a Távoli asztalt, miután az .rdp fájlt kapja.</span><span class="sxs-lookup"><span data-stu-id="4fe18-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="4fe18-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="4fe18-118">-LocalPath</span></span>
<span data-ttu-id="4fe18-119">Megadja azt a helyi teljes elérési utat, ahol ez a parancsmag a .rdp fájlt tárolja.</span><span class="sxs-lookup"><span data-stu-id="4fe18-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="4fe18-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4fe18-120">-Name</span></span>
<span data-ttu-id="4fe18-121">Megadja annak az elérhetőségi készletnek a nevét, amelybe ez a parancsmag be lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="4fe18-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4fe18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe18-122">-ResourceGroupName</span></span>
<span data-ttu-id="4fe18-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fe18-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4fe18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe18-124">CommonParameters</span></span>
<span data-ttu-id="4fe18-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe18-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fe18-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe18-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fe18-127">INPUTS</span></span>

### <span data-ttu-id="4fe18-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4fe18-128">System.String</span></span>

## <span data-ttu-id="4fe18-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fe18-129">OUTPUTS</span></span>

### <span data-ttu-id="4fe18-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="4fe18-130">System.Void</span></span>

## <span data-ttu-id="4fe18-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4fe18-131">NOTES</span></span>

## <span data-ttu-id="4fe18-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fe18-132">RELATED LINKS</span></span>
