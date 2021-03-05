---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: 28f1486375e0efc1f9b1b3f9a18f12050dafd799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002134"
---
# <span data-ttu-id="c8796-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8796-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="c8796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8796-102">SYNOPSIS</span></span>
<span data-ttu-id="c8796-103">Létrehozza a Synapse Analytics munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="c8796-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="c8796-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8796-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8796-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8796-105">DESCRIPTION</span></span>
<span data-ttu-id="c8796-106">A **New-AzSynapseWorkspace** parancsmag létrehoz egy Azure Synapse Analytics-munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="c8796-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="c8796-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8796-107">EXAMPLES</span></span>

### <span data-ttu-id="c8796-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c8796-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="c8796-109">Ez a parancs létrehoz egy ContosoWorkspace nevű Synapse Analytics munkaterületet, amely a ContosoAdlGenStorage adattárat használja a ContosoResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c8796-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c8796-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8796-110">PARAMETERS</span></span>

### <span data-ttu-id="c8796-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8796-111">-AsJob</span></span>
<span data-ttu-id="c8796-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c8796-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8796-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8796-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="c8796-114">Az alapértelmezett ADLS Gen2 tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="c8796-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="c8796-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="c8796-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="c8796-116">Az alapértelmezett ADLS Gen2 fájlrendszer.</span><span class="sxs-lookup"><span data-stu-id="c8796-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="c8796-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8796-117">-DefaultProfile</span></span>
<span data-ttu-id="c8796-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8796-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8796-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c8796-119">-Location</span></span>
<span data-ttu-id="c8796-120">Azure-régió, ahol az erőforrást létre kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="c8796-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="c8796-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8796-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="c8796-122">Az Azure Synapse munkaterülethez dedikált, Szinapszis által felügyelt virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="c8796-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="c8796-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c8796-123">-Name</span></span>
<span data-ttu-id="c8796-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="c8796-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c8796-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8796-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8796-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c8796-126">Resource group name.</span></span>

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

### <span data-ttu-id="c8796-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="c8796-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="c8796-128">SQL-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="c8796-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="c8796-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8796-129">-Tag</span></span>
<span data-ttu-id="c8796-130">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="c8796-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="c8796-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8796-131">-Confirm</span></span>
<span data-ttu-id="c8796-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c8796-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8796-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8796-133">-WhatIf</span></span>
<span data-ttu-id="c8796-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c8796-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8796-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8796-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8796-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8796-136">CommonParameters</span></span>
<span data-ttu-id="c8796-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8796-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8796-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8796-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8796-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8796-139">INPUTS</span></span>

### <span data-ttu-id="c8796-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c8796-140">System.String</span></span>

### <span data-ttu-id="c8796-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c8796-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c8796-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="c8796-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="c8796-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8796-143">OUTPUTS</span></span>

### <span data-ttu-id="c8796-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8796-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c8796-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8796-145">NOTES</span></span>

## <span data-ttu-id="c8796-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8796-146">RELATED LINKS</span></span>
