---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: dcd8d4164d091564aef3d3802430ab499eac38ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182809"
---
# <span data-ttu-id="e30f5-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e30f5-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="e30f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e30f5-102">SYNOPSIS</span></span>
<span data-ttu-id="e30f5-103">Tárgyi forrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="e30f5-103">Creates an artifact source.</span></span>

## <span data-ttu-id="e30f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e30f5-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e30f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e30f5-105">DESCRIPTION</span></span>
<span data-ttu-id="e30f5-106">A **New-AzDeploymentManagerArtifactSource** parancsmag tárgyi forrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e30f5-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="e30f5-107">Adja meg a *nevet* , a *ResourceGroupName* és a szükséges tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e30f5-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="e30f5-108">A visszaadott objektumot helyileg módosíthatja, majd a Set-AzDeploymentManagerArtifactSource parancsmag használatával alkalmazhatja a módosításokat az objektum forrására.</span><span class="sxs-lookup"><span data-stu-id="e30f5-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="e30f5-109">A parancsmag egy olyan ArtifactSource objektumot ad eredményül, amely ResourceId hivatkozik az New-AzDeploymentManagerServiceTopology parancsmagban, így a ServiceUnit-erőforrásokhoz, a sablon-és a Parameters-fájlokhoz szükséges leletek is hivatkozhatók erre a helyről.</span><span class="sxs-lookup"><span data-stu-id="e30f5-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="e30f5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e30f5-110">EXAMPLES</span></span>

### <span data-ttu-id="e30f5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e30f5-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="e30f5-112">A ContosoResourceGroup a ContosoArtifactSource nevű tárgyi forrást hozza létre az erőforrás helyére.</span><span class="sxs-lookup"><span data-stu-id="e30f5-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="e30f5-113">A SasUri tulajdonság egy Azure Storage SAS URI azonosítóval rendelkezik annak a tárolónak a tárolójában, ahol a leletek vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="e30f5-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="e30f5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e30f5-114">PARAMETERS</span></span>

### <span data-ttu-id="e30f5-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="e30f5-115">-ArtifactRoot</span></span>
<span data-ttu-id="e30f5-116">A nem kötelező könyvtár a leletek tárolójában.</span><span class="sxs-lookup"><span data-stu-id="e30f5-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="e30f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30f5-117">-DefaultProfile</span></span>
<span data-ttu-id="e30f5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e30f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e30f5-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="e30f5-119">-Location</span></span>
<span data-ttu-id="e30f5-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e30f5-120">The location of the resource.</span></span>

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

### <span data-ttu-id="e30f5-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e30f5-121">-Name</span></span>
<span data-ttu-id="e30f5-122">A tárgy forrásának neve.</span><span class="sxs-lookup"><span data-stu-id="e30f5-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="e30f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="e30f5-124">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="e30f5-124">The resource group.</span></span>

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

### <span data-ttu-id="e30f5-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="e30f5-125">-SasUri</span></span>
<span data-ttu-id="e30f5-126">A SAS-URI az Azure Storage tárolóhoz, ahol a leletek vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="e30f5-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="e30f5-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="e30f5-127">-Tag</span></span>
<span data-ttu-id="e30f5-128">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="e30f5-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e30f5-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e30f5-129">-Confirm</span></span>
<span data-ttu-id="e30f5-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e30f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e30f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e30f5-131">-WhatIf</span></span>
<span data-ttu-id="e30f5-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e30f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e30f5-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e30f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e30f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30f5-134">CommonParameters</span></span>
<span data-ttu-id="e30f5-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e30f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30f5-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e30f5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30f5-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e30f5-137">INPUTS</span></span>

### <span data-ttu-id="e30f5-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e30f5-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e30f5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e30f5-139">OUTPUTS</span></span>

### <span data-ttu-id="e30f5-140">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e30f5-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="e30f5-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e30f5-141">NOTES</span></span>

## <span data-ttu-id="e30f5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e30f5-142">RELATED LINKS</span></span>
