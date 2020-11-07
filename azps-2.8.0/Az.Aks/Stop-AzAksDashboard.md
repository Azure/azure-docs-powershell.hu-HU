---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 4d4e2a86bfa2974cabcc4208f7a314019f5804e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668195"
---
# <span data-ttu-id="22cb9-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="22cb9-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="22cb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="22cb9-103">Állítsa le a Kubectl SSH-alagutat a Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="22cb9-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="22cb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22cb9-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22cb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="22cb9-106">Állítsa le a Kubectl SSH-alagutat a Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="22cb9-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="22cb9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="22cb9-107">EXAMPLES</span></span>

### <span data-ttu-id="22cb9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="22cb9-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="22cb9-109">A meglévő SSH bújtatási beállítás leállítása a Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="22cb9-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="22cb9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22cb9-110">PARAMETERS</span></span>

### <span data-ttu-id="22cb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cb9-111">-DefaultProfile</span></span>
<span data-ttu-id="22cb9-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22cb9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cb9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22cb9-113">-PassThru</span></span>
<span data-ttu-id="22cb9-114">Igaz értéket ad eredményül, ha az SSH bújtatás be van zárva.</span><span class="sxs-lookup"><span data-stu-id="22cb9-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="22cb9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cb9-115">CommonParameters</span></span>
<span data-ttu-id="22cb9-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22cb9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cb9-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22cb9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cb9-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22cb9-118">INPUTS</span></span>

### <span data-ttu-id="22cb9-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="22cb9-119">None</span></span>

## <span data-ttu-id="22cb9-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22cb9-120">OUTPUTS</span></span>

### <span data-ttu-id="22cb9-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22cb9-121">System.Boolean</span></span>

## <span data-ttu-id="22cb9-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22cb9-122">NOTES</span></span>

## <span data-ttu-id="22cb9-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22cb9-123">RELATED LINKS</span></span>
