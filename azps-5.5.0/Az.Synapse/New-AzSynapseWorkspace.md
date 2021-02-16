---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162826"
---
# <span data-ttu-id="74354-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="74354-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="74354-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74354-102">SYNOPSIS</span></span>
<span data-ttu-id="74354-103">Létrehozza a Synapse Analytics munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="74354-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="74354-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74354-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74354-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74354-105">DESCRIPTION</span></span>
<span data-ttu-id="74354-106">A **New-AzSynapseWorkspace** parancsmag létrehoz egy Azure Synapse Analytics-munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="74354-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="74354-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74354-107">EXAMPLES</span></span>

### <span data-ttu-id="74354-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="74354-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="74354-109">Ez a parancs létrehoz egy ContosoWorkspace nevű Synapse Analytics munkaterületet, amely a ContosoAdlGenStorage adattárat használja a ContosoResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="74354-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="74354-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74354-110">PARAMETERS</span></span>

### <span data-ttu-id="74354-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74354-111">-AsJob</span></span>
<span data-ttu-id="74354-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="74354-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74354-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="74354-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="74354-114">Az alapértelmezett ADLS Gen2 tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="74354-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74354-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="74354-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="74354-116">Az alapértelmezett ADLS Gen2 fájlrendszer.</span><span class="sxs-lookup"><span data-stu-id="74354-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74354-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74354-117">-DefaultProfile</span></span>
<span data-ttu-id="74354-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74354-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74354-119">-Location</span><span class="sxs-lookup"><span data-stu-id="74354-119">-Location</span></span>
<span data-ttu-id="74354-120">Azure-régió, ahol az erőforrást létre kell hoznunk.</span><span class="sxs-lookup"><span data-stu-id="74354-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74354-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="74354-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="74354-122">Az Azure Synapse munkaterülethez dedikált, Szinapszis által felügyelt virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="74354-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74354-123">-Name</span><span class="sxs-lookup"><span data-stu-id="74354-123">-Name</span></span>
<span data-ttu-id="74354-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="74354-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74354-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74354-125">-ResourceGroupName</span></span>
<span data-ttu-id="74354-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="74354-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74354-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="74354-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="74354-128">SQL-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="74354-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74354-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="74354-129">-Tag</span></span>
<span data-ttu-id="74354-130">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="74354-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74354-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74354-131">-Confirm</span></span>
<span data-ttu-id="74354-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="74354-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74354-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74354-133">-WhatIf</span></span>
<span data-ttu-id="74354-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="74354-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74354-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74354-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74354-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74354-136">CommonParameters</span></span>
<span data-ttu-id="74354-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74354-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74354-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74354-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74354-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74354-139">INPUTS</span></span>

### <span data-ttu-id="74354-140">System.String</span><span class="sxs-lookup"><span data-stu-id="74354-140">System.String</span></span>

### <span data-ttu-id="74354-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="74354-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="74354-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="74354-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="74354-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74354-143">OUTPUTS</span></span>

### <span data-ttu-id="74354-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="74354-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="74354-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74354-145">NOTES</span></span>

## <span data-ttu-id="74354-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74354-146">RELATED LINKS</span></span>
