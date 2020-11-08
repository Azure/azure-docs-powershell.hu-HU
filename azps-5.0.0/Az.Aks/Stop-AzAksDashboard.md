---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187099"
---
# <span data-ttu-id="32fbb-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="32fbb-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="32fbb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="32fbb-103">Állítsa le a Kubectl SSH-alagutat a Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="32fbb-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="32fbb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32fbb-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32fbb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="32fbb-106">Állítsa le a Kubectl SSH-alagutat a Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="32fbb-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="32fbb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="32fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="32fbb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="32fbb-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="32fbb-109">A meglévő SSH bújtatási beállítás leállítása a Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="32fbb-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="32fbb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32fbb-110">PARAMETERS</span></span>

### <span data-ttu-id="32fbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fbb-111">-DefaultProfile</span></span>
<span data-ttu-id="32fbb-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32fbb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32fbb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32fbb-113">-PassThru</span></span>
<span data-ttu-id="32fbb-114">Igaz értéket ad eredményül, ha az SSH bújtatás be van zárva.</span><span class="sxs-lookup"><span data-stu-id="32fbb-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="32fbb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fbb-115">CommonParameters</span></span>
<span data-ttu-id="32fbb-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32fbb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fbb-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="32fbb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fbb-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32fbb-118">INPUTS</span></span>

### <span data-ttu-id="32fbb-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="32fbb-119">None</span></span>

## <span data-ttu-id="32fbb-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32fbb-120">OUTPUTS</span></span>

### <span data-ttu-id="32fbb-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32fbb-121">System.Boolean</span></span>

## <span data-ttu-id="32fbb-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32fbb-122">NOTES</span></span>

## <span data-ttu-id="32fbb-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32fbb-123">RELATED LINKS</span></span>