---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210023"
---
# <span data-ttu-id="93bad-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="93bad-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="93bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93bad-102">SYNOPSIS</span></span>
<span data-ttu-id="93bad-103">Eltávolít egy ügynökkészlet-profilt egy tárolószolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="93bad-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="93bad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93bad-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93bad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93bad-105">DESCRIPTION</span></span>
<span data-ttu-id="93bad-106">A **Remove-AzContainerServiceAgentPoolProfile** parancsmag eltávolít egy ügynökkészlet-profilt egy tárolószolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="93bad-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="93bad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93bad-107">EXAMPLES</span></span>

### <span data-ttu-id="93bad-108">1. példa: Profil eltávolítása egy tárolószolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="93bad-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="93bad-109">Az első parancs egy CSResourceGroup17 nevű tárolószolgáltatást kap a Get-AzContainerService parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="93bad-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="93bad-110">A parancs a szolgáltatást a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="93bad-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="93bad-111">A második parancs eltávolítja az AgentPool01 nevű profilt a $Container.</span><span class="sxs-lookup"><span data-stu-id="93bad-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="93bad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93bad-112">PARAMETERS</span></span>

### <span data-ttu-id="93bad-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="93bad-113">-ContainerService</span></span>
<span data-ttu-id="93bad-114">Azt a tárolószolgáltatás-objektumot adja meg, amelyből a parancsmag eltávolítja az ügynökkészlet-profilt.</span><span class="sxs-lookup"><span data-stu-id="93bad-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93bad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bad-115">-DefaultProfile</span></span>
<span data-ttu-id="93bad-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93bad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93bad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="93bad-117">-Name</span></span>
<span data-ttu-id="93bad-118">Annak az ügynökkészlet-profilnak a neve, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="93bad-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93bad-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93bad-119">-Confirm</span></span>
<span data-ttu-id="93bad-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93bad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93bad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93bad-121">-WhatIf</span></span>
<span data-ttu-id="93bad-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93bad-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93bad-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93bad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93bad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bad-124">CommonParameters</span></span>
<span data-ttu-id="93bad-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93bad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bad-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93bad-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bad-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93bad-127">INPUTS</span></span>

### <span data-ttu-id="93bad-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="93bad-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="93bad-129">System.String</span><span class="sxs-lookup"><span data-stu-id="93bad-129">System.String</span></span>

## <span data-ttu-id="93bad-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93bad-130">OUTPUTS</span></span>

### <span data-ttu-id="93bad-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="93bad-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="93bad-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93bad-132">NOTES</span></span>

## <span data-ttu-id="93bad-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93bad-133">RELATED LINKS</span></span>

[<span data-ttu-id="93bad-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="93bad-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="93bad-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="93bad-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


