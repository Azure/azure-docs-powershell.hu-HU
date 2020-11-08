---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195780"
---
# <span data-ttu-id="0355f-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="0355f-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="0355f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0355f-102">SYNOPSIS</span></span>
<span data-ttu-id="0355f-103">Módszer egy áttelepítési projekt beszerzésére</span><span class="sxs-lookup"><span data-stu-id="0355f-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="0355f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0355f-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0355f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0355f-105">DESCRIPTION</span></span>
<span data-ttu-id="0355f-106">Módszer egy áttelepítési projekt beszerzésére</span><span class="sxs-lookup"><span data-stu-id="0355f-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="0355f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0355f-107">EXAMPLES</span></span>

### <span data-ttu-id="0355f-108">Példa 1: Get</span><span class="sxs-lookup"><span data-stu-id="0355f-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="0355f-109">Módszer egy áttelepítési projekt beszerzésére</span><span class="sxs-lookup"><span data-stu-id="0355f-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="0355f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0355f-110">PARAMETERS</span></span>

### <span data-ttu-id="0355f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0355f-111">-DefaultProfile</span></span>
<span data-ttu-id="0355f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0355f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0355f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0355f-113">-Name</span></span>
<span data-ttu-id="0355f-114">Az Azure áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="0355f-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0355f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0355f-115">-ResourceGroupName</span></span>
<span data-ttu-id="0355f-116">Annak a programnak a neve, amely a projectet Áttelepítő Azure Resource Group része.</span><span class="sxs-lookup"><span data-stu-id="0355f-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="0355f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0355f-117">-SubscriptionId</span></span>
<span data-ttu-id="0355f-118">Azure-előfizetési azonosító, amelybe a projekt-áttelepítést hozta létre.</span><span class="sxs-lookup"><span data-stu-id="0355f-118">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0355f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0355f-119">CommonParameters</span></span>
<span data-ttu-id="0355f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0355f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0355f-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0355f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0355f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0355f-122">INPUTS</span></span>

## <span data-ttu-id="0355f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0355f-123">OUTPUTS</span></span>

### <span data-ttu-id="0355f-124">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="0355f-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="0355f-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0355f-125">NOTES</span></span>

<span data-ttu-id="0355f-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0355f-126">ALIASES</span></span>

## <span data-ttu-id="0355f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0355f-127">RELATED LINKS</span></span>

