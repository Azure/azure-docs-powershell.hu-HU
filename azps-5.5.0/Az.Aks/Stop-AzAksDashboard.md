---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159874"
---
# <span data-ttu-id="cbe93-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="cbe93-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="cbe93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe93-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe93-103">Állítsa le a Start-AzKubernetesDashboardban létrehozott Kutectl SSH-csatornát.</span><span class="sxs-lookup"><span data-stu-id="cbe93-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="cbe93-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbe93-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbe93-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbe93-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe93-106">Állítsa le a Start-AzKubernetesDashboardban létrehozott Kutectl SSH-csatornát.</span><span class="sxs-lookup"><span data-stu-id="cbe93-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="cbe93-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbe93-107">EXAMPLES</span></span>

### <span data-ttu-id="cbe93-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cbe93-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="cbe93-109">A Start-AzKubernetesDashboard futtatásával leállítja a meglévő SSH-telepítő telepítőt.</span><span class="sxs-lookup"><span data-stu-id="cbe93-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="cbe93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbe93-110">PARAMETERS</span></span>

### <span data-ttu-id="cbe93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe93-111">-DefaultProfile</span></span>
<span data-ttu-id="cbe93-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbe93-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe93-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbe93-113">-PassThru</span></span>
<span data-ttu-id="cbe93-114">Igaz értéket ad vissza, ha az SSH-átjáró be van zárva.</span><span class="sxs-lookup"><span data-stu-id="cbe93-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="cbe93-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe93-115">CommonParameters</span></span>
<span data-ttu-id="cbe93-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe93-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe93-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbe93-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe93-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbe93-118">INPUTS</span></span>

### <span data-ttu-id="cbe93-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="cbe93-119">None</span></span>

## <span data-ttu-id="cbe93-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbe93-120">OUTPUTS</span></span>

### <span data-ttu-id="cbe93-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbe93-121">System.Boolean</span></span>

## <span data-ttu-id="cbe93-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbe93-122">NOTES</span></span>

## <span data-ttu-id="cbe93-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbe93-123">RELATED LINKS</span></span>
