---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 8aab061d7f61605273bd7147dc5a85ca45bf8ad0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925777"
---
# <span data-ttu-id="590aa-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="590aa-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="590aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="590aa-102">SYNOPSIS</span></span>
<span data-ttu-id="590aa-103">Összetevőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="590aa-103">Creates an artifact source.</span></span>

## <span data-ttu-id="590aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="590aa-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="590aa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="590aa-105">DESCRIPTION</span></span>
<span data-ttu-id="590aa-106">A **New-AzDeploymentManagerArtifactSource** parancsmag létrehoz egy összetevőforrást.</span><span class="sxs-lookup"><span data-stu-id="590aa-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="590aa-107">Adja meg *a Name*, *ResourceGroupName és* a kötelező tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="590aa-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="590aa-108">A visszaadott objektumot helyben módosíthatja, majd a módosításokat alkalmazhatja az objektumforrásra a Set-AzDeploymentManagerArtifactSource parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="590aa-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="590aa-109">A parancsmag egy ResourceId objektumot ad vissza, amelyre hivatkozhat a New-AzDeploymentManagerServiceTopology-parancsmagban, így innen hivatkozhat a ServiceUnit-erőforráshoz, a Sablon és a Parameters fájlokhoz szükséges objektumokra.</span><span class="sxs-lookup"><span data-stu-id="590aa-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="590aa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="590aa-110">EXAMPLES</span></span>

### <span data-ttu-id="590aa-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="590aa-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="590aa-112">A ContosoResourceGroupban létrehoz egy, a ContosoArtifactSource nevű összetevőt az erőforrás helyeként.</span><span class="sxs-lookup"><span data-stu-id="590aa-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="590aa-113">A SasUri tulajdonság egy Azure Storage SAS Uri-t biztosít a tártárolóhoz, ahol az összetevők találhatók.</span><span class="sxs-lookup"><span data-stu-id="590aa-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="590aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="590aa-114">PARAMETERS</span></span>

### <span data-ttu-id="590aa-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="590aa-115">-ArtifactRoot</span></span>
<span data-ttu-id="590aa-116">Az opcionális címtáreltolás az objektumtár tárolója alatt.</span><span class="sxs-lookup"><span data-stu-id="590aa-116">The optional directory offset under the storage container for the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="590aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590aa-117">-DefaultProfile</span></span>
<span data-ttu-id="590aa-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="590aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="590aa-119">-Location</span><span class="sxs-lookup"><span data-stu-id="590aa-119">-Location</span></span>
<span data-ttu-id="590aa-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="590aa-120">The location of the resource.</span></span>

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

### <span data-ttu-id="590aa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="590aa-121">-Name</span></span>
<span data-ttu-id="590aa-122">Az összetevő-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="590aa-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="590aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="590aa-124">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="590aa-124">The resource group.</span></span>

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

### <span data-ttu-id="590aa-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="590aa-125">-SasUri</span></span>
<span data-ttu-id="590aa-126">Az SAS Uri az Azure tárolóhoz, ahol az összetevők vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="590aa-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="590aa-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="590aa-127">-Tag</span></span>
<span data-ttu-id="590aa-128">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="590aa-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="590aa-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="590aa-129">-Confirm</span></span>
<span data-ttu-id="590aa-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="590aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="590aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="590aa-131">-WhatIf</span></span>
<span data-ttu-id="590aa-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="590aa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="590aa-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="590aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="590aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590aa-134">CommonParameters</span></span>
<span data-ttu-id="590aa-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590aa-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="590aa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590aa-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="590aa-137">INPUTS</span></span>

### <span data-ttu-id="590aa-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="590aa-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="590aa-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="590aa-139">OUTPUTS</span></span>

### <span data-ttu-id="590aa-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="590aa-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="590aa-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="590aa-141">NOTES</span></span>

## <span data-ttu-id="590aa-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="590aa-142">RELATED LINKS</span></span>
