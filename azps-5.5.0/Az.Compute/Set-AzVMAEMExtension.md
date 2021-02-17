---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209974"
---
# <span data-ttu-id="d4a1f-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4a1f-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="d4a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a1f-103">Támogatja az SAP-rendszerek figyelési funkcióját.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="d4a1f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4a1f-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a1f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a1f-106">A **Set-AzVMAEMExtension** parancsmag frissíti egy virtuális gép konfigurációját a virtuális gépre telepített SAP-rendszerek figyelési ellenőrzésére vonatkozó támogatás engedélyezéséhez vagy frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="d4a1f-107">A parancsmag telepíti az Azure Enhanced Monitoring (AEM) bővítményt, amely összegyűjti a teljesítményadatokat, és felderíthetővé teszi azt az SAP rendszer számára.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="d4a1f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4a1f-108">EXAMPLES</span></span>

### <span data-ttu-id="d4a1f-109">1. példa: Az AEM bővítmény használata</span><span class="sxs-lookup"><span data-stu-id="d4a1f-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="d4a1f-110">Ez a parancs beállítja a contoso-kiszolgáló nevű virtuális gépet az AEM-bővítmény használatára.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="d4a1f-111">A parancs megadja az stdstorage nevű tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="d4a1f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4a1f-112">PARAMETERS</span></span>

### <span data-ttu-id="d4a1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a1f-113">-DefaultProfile</span></span>
<span data-ttu-id="d4a1f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4a1f-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="d4a1f-115">-EnableWAD</span></span>
<span data-ttu-id="d4a1f-116">Ha meg van adva ez a paraméter, a parancsmag engedélyezi a Windows Azure diagnosztika funkcióját ehhez a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="d4a1f-117">-InstallNewExtension</span></span>
<span data-ttu-id="d4a1f-118">Telepítse az új VM-bővítményt az SAP-hoz.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d4a1f-119">-NoWait</span></span>
<span data-ttu-id="d4a1f-120">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d4a1f-121">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="d4a1f-122">-OSType</span></span>
<span data-ttu-id="d4a1f-123">Az operációs rendszer lemezének típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d4a1f-124">Ha az operációs rendszer lemezének nincs típusa, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d4a1f-125">A paraméter elfogadható értékei a következőek: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a1f-126">-ResourceGroupName</span></span>
<span data-ttu-id="d4a1f-127">Annak a virtuális gépnek a nevét adja meg, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d4a1f-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="d4a1f-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="d4a1f-129">Beállítja a VIRTUÁLIS GÉP-identitás hozzáférését az egyes erőforrásokhoz, például az adatlemezekhez a teljes erőforráscsoport helyett.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="d4a1f-130">-SkipStorage</span></span>
<span data-ttu-id="d4a1f-131">Azt jelzi, hogy ez a parancsmag kihagyja a tárterület konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4a1f-132">-VMName</span></span>
<span data-ttu-id="d4a1f-133">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d4a1f-134">Ez a parancsmag hozzáadja az AEM bővítményt a paraméter által megadott virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d4a1f-135">-WADStorageAccountName</span></span>
<span data-ttu-id="d4a1f-136">Annak a tárfióknak a nevét adja meg, amelyből a parancsmag a LinuxDiagnostics vagy az IaaSDiagnostics bővítményt konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="d4a1f-137">Ha a virtuális gép nem használ szokásos tárfiókot, meg kell adnia a paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a1f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a1f-138">CommonParameters</span></span>
<span data-ttu-id="d4a1f-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a1f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a1f-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4a1f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a1f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a1f-141">INPUTS</span></span>

### <span data-ttu-id="d4a1f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d4a1f-142">System.String</span></span>

## <span data-ttu-id="d4a1f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4a1f-143">OUTPUTS</span></span>

### <span data-ttu-id="d4a1f-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d4a1f-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d4a1f-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4a1f-145">NOTES</span></span>

## <span data-ttu-id="d4a1f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4a1f-146">RELATED LINKS</span></span>

[<span data-ttu-id="d4a1f-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4a1f-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="d4a1f-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4a1f-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="d4a1f-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4a1f-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


