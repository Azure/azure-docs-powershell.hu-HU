---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155995"
---
# <span data-ttu-id="b3f42-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b3f42-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b3f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3f42-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f42-103">Azure AD-rendszergazdát biztosít a Synapse Analytics SQL-készlethez.</span><span class="sxs-lookup"><span data-stu-id="b3f42-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b3f42-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3f42-104">SYNTAX</span></span>

### <span data-ttu-id="b3f42-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3f42-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3f42-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3f42-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3f42-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3f42-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3f42-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3f42-108">DESCRIPTION</span></span>
<span data-ttu-id="b3f42-109">A **Set-AzSynapseSqlActiveDirectoryAdministrator** parancsmag azure Active Directory (Azure AD) rendszergazdát biztosít az Azure Synapse Analytics Workspace szolgáltatáshoz az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b3f42-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="b3f42-110">Egyszerre csak egy rendszergazda létesíthet.</span><span class="sxs-lookup"><span data-stu-id="b3f42-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="b3f42-111">Az Azure AD következő tagjait lehet kiépítve a Synapse Analytics Workspace rendszergazdájaként:</span><span class="sxs-lookup"><span data-stu-id="b3f42-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="b3f42-112">Az Azure AD natív tagjai</span><span class="sxs-lookup"><span data-stu-id="b3f42-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="b3f42-113">Az Azure AD összevont tagjai</span><span class="sxs-lookup"><span data-stu-id="b3f42-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="b3f42-114">Importált tagok más Azure AD-ről, akik natív vagy összevont tagok</span><span class="sxs-lookup"><span data-stu-id="b3f42-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="b3f42-115">A Microsoft-fiókokként létrehozott Azure AD-csoportokat ( például a Outlook.com-, Hotmail.com- vagy Live.com-tartományokat ) nem lehet rendszergazdaként támogatni.</span><span class="sxs-lookup"><span data-stu-id="b3f42-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="b3f42-116">Más vendégfiókok, például a Gmail.com vagy Yahoo.com tartományában található fiókok, nem támogatottak rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="b3f42-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="b3f42-117">Azt javasoljuk, hogy rendszergazdaként kiépítsen egy dedikált Azure AD-csoportot.</span><span class="sxs-lookup"><span data-stu-id="b3f42-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="b3f42-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3f42-118">EXAMPLES</span></span>

### <span data-ttu-id="b3f42-119">1. példa</span><span class="sxs-lookup"><span data-stu-id="b3f42-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="b3f42-120">Ez a parancs egy DBAs nevű Azure AD-rendszergazdai csoportot hoz létre a ContosoWorkspace nevű munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="b3f42-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b3f42-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="b3f42-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="b3f42-122">Ez a parancs egy DBAs nevű Azure AD-rendszergazdai csoportot hoz létre a ContosoWorkspace nevű munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="b3f42-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="b3f42-123">Ez akkor is sikeres lesz, ha a csoport megjelenítendő neve nem egyedi.</span><span class="sxs-lookup"><span data-stu-id="b3f42-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="b3f42-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3f42-124">PARAMETERS</span></span>

### <span data-ttu-id="b3f42-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3f42-125">-AsJob</span></span>
<span data-ttu-id="b3f42-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b3f42-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3f42-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f42-127">-DefaultProfile</span></span>
<span data-ttu-id="b3f42-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3f42-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f42-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b3f42-129">-DisplayName</span></span>
<span data-ttu-id="b3f42-130">Annak a felhasználónak vagy csoportnak a megjelenítendő nevét adja meg, akinek engedélyt kell kiadó felhasználó vagy csoport.</span><span class="sxs-lookup"><span data-stu-id="b3f42-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="b3f42-131">Ennek a megjelenítendő névnek az aktuális előfizetéshez társított Active Directoryban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b3f42-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f42-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3f42-132">-InputObject</span></span>
<span data-ttu-id="b3f42-133">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="b3f42-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f42-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3f42-134">-ObjectId</span></span>
<span data-ttu-id="b3f42-135">Annak a felhasználónak vagy csoportnak az objektumazonosítóját adja meg az Azure Active Directoryban, amelynek vagy amelynek az engedélyét ki kell adni.</span><span class="sxs-lookup"><span data-stu-id="b3f42-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f42-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f42-136">-ResourceGroupName</span></span>
<span data-ttu-id="b3f42-137">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3f42-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f42-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3f42-138">-ResourceId</span></span>
<span data-ttu-id="b3f42-139">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3f42-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f42-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b3f42-140">-WorkspaceName</span></span>
<span data-ttu-id="b3f42-141">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="b3f42-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f42-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3f42-142">-Confirm</span></span>
<span data-ttu-id="b3f42-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b3f42-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f42-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f42-144">-WhatIf</span></span>
<span data-ttu-id="b3f42-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b3f42-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f42-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3f42-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f42-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f42-147">CommonParameters</span></span>
<span data-ttu-id="b3f42-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f42-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f42-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3f42-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f42-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3f42-150">INPUTS</span></span>

### <span data-ttu-id="b3f42-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b3f42-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b3f42-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3f42-152">OUTPUTS</span></span>

### <span data-ttu-id="b3f42-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="b3f42-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="b3f42-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3f42-154">NOTES</span></span>

## <span data-ttu-id="b3f42-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3f42-155">RELATED LINKS</span></span>
