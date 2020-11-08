---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025636"
---
# <span data-ttu-id="45526-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="45526-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="45526-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45526-102">SYNOPSIS</span></span>
<span data-ttu-id="45526-103">A szinapszis Analytics-munkaterületet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="45526-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="45526-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45526-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45526-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45526-105">DESCRIPTION</span></span>
<span data-ttu-id="45526-106">A **New-AzSynapseWorkspace** parancsmag az Azure szinapszis Analytics-munkaterületet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="45526-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="45526-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45526-107">EXAMPLES</span></span>

### <span data-ttu-id="45526-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45526-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="45526-109">Ez a parancs létrehoz egy ContosoWorkspace nevű szinapszis-elemzési munkaterületet, amely az ContosoAdlGenStorage-adattárolót használja, a ContosoResourceGroup nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="45526-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="45526-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45526-110">PARAMETERS</span></span>

### <span data-ttu-id="45526-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45526-111">-AsJob</span></span>
<span data-ttu-id="45526-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="45526-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45526-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="45526-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="45526-114">Az alapértelmezett ADLS Gen2-tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="45526-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="45526-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="45526-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="45526-116">Az alapértelmezett ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="45526-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="45526-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45526-117">-DefaultProfile</span></span>
<span data-ttu-id="45526-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45526-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45526-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="45526-119">-Location</span></span>
<span data-ttu-id="45526-120">Az Azure régió, ahol az erőforrást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="45526-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="45526-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="45526-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="45526-122">Az Azure szinapszis-munkaterülethez rendelt, Szinapszisral felügyelt virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="45526-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="45526-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45526-123">-Name</span></span>
<span data-ttu-id="45526-124">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="45526-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="45526-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45526-125">-ResourceGroupName</span></span>
<span data-ttu-id="45526-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="45526-126">Resource group name.</span></span>

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

### <span data-ttu-id="45526-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="45526-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="45526-128">SQL-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="45526-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="45526-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="45526-129">-Tag</span></span>
<span data-ttu-id="45526-130">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="45526-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="45526-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45526-131">-Confirm</span></span>
<span data-ttu-id="45526-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45526-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45526-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45526-133">-WhatIf</span></span>
<span data-ttu-id="45526-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45526-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45526-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45526-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45526-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45526-136">CommonParameters</span></span>
<span data-ttu-id="45526-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45526-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45526-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45526-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45526-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45526-139">INPUTS</span></span>

### <span data-ttu-id="45526-140">System. String</span><span class="sxs-lookup"><span data-stu-id="45526-140">System.String</span></span>

### <span data-ttu-id="45526-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="45526-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="45526-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="45526-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="45526-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45526-143">OUTPUTS</span></span>

### <span data-ttu-id="45526-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="45526-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="45526-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45526-145">NOTES</span></span>

## <span data-ttu-id="45526-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45526-146">RELATED LINKS</span></span>
