---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 633173a0ce8814ee2af9300be5b1cfc19bdf9a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930433"
---
# <span data-ttu-id="ea5e9-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="ea5e9-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="ea5e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5e9-103">Állítsa le a Start-AzKubernetesDashboardban létrehozott Kutectl SSH-csatornát.</span><span class="sxs-lookup"><span data-stu-id="ea5e9-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="ea5e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea5e9-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea5e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea5e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5e9-106">Állítsa le a Start-AzKubernetesDashboardban létrehozott Kutectl SSH-csatornát.</span><span class="sxs-lookup"><span data-stu-id="ea5e9-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="ea5e9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea5e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ea5e9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea5e9-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="ea5e9-109">A Start-AzKubernetesDashboard futtatásával leállítja a meglévő SSH-telepítő telepítőt.</span><span class="sxs-lookup"><span data-stu-id="ea5e9-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="ea5e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea5e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ea5e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ea5e9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea5e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea5e9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea5e9-113">-PassThru</span></span>
<span data-ttu-id="ea5e9-114">Igaz értéket ad vissza, ha az SSH-átjáró be van zárva.</span><span class="sxs-lookup"><span data-stu-id="ea5e9-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="ea5e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5e9-115">CommonParameters</span></span>
<span data-ttu-id="ea5e9-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5e9-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea5e9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5e9-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea5e9-118">INPUTS</span></span>

### <span data-ttu-id="ea5e9-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="ea5e9-119">None</span></span>

## <span data-ttu-id="ea5e9-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea5e9-120">OUTPUTS</span></span>

### <span data-ttu-id="ea5e9-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea5e9-121">System.Boolean</span></span>

## <span data-ttu-id="ea5e9-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea5e9-122">NOTES</span></span>

## <span data-ttu-id="ea5e9-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea5e9-123">RELATED LINKS</span></span>
