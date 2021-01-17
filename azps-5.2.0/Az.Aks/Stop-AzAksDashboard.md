---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335777"
---
# <span data-ttu-id="7f9db-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="7f9db-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="7f9db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f9db-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9db-103">Állítsa le a Start-AzKubernetesDashboardban létrehozott Kutectl SSH-csatornát.</span><span class="sxs-lookup"><span data-stu-id="7f9db-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="7f9db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f9db-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f9db-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f9db-105">DESCRIPTION</span></span>
<span data-ttu-id="7f9db-106">Állítsa le a Start-AzKubernetesDashboardban létrehozott Kutectl SSH-csatornát.</span><span class="sxs-lookup"><span data-stu-id="7f9db-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="7f9db-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f9db-107">EXAMPLES</span></span>

### <span data-ttu-id="7f9db-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7f9db-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="7f9db-109">A Start-AzKubernetesDashboard futtatásával leállítja a meglévő SSH-telepítő telepítőt.</span><span class="sxs-lookup"><span data-stu-id="7f9db-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="7f9db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f9db-110">PARAMETERS</span></span>

### <span data-ttu-id="7f9db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9db-111">-DefaultProfile</span></span>
<span data-ttu-id="7f9db-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f9db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f9db-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f9db-113">-PassThru</span></span>
<span data-ttu-id="7f9db-114">Igaz értéket ad vissza, ha az SSH-átjáró be van zárva.</span><span class="sxs-lookup"><span data-stu-id="7f9db-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="7f9db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9db-115">CommonParameters</span></span>
<span data-ttu-id="7f9db-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f9db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9db-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f9db-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9db-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f9db-118">INPUTS</span></span>

### <span data-ttu-id="7f9db-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="7f9db-119">None</span></span>

## <span data-ttu-id="7f9db-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f9db-120">OUTPUTS</span></span>

### <span data-ttu-id="7f9db-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f9db-121">System.Boolean</span></span>

## <span data-ttu-id="7f9db-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f9db-122">NOTES</span></span>

## <span data-ttu-id="7f9db-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f9db-123">RELATED LINKS</span></span>
