---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 4ec1c8c2788469ffd377127bc58f657c817434a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500651"
---
# <span data-ttu-id="342f3-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="342f3-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="342f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="342f3-102">SYNOPSIS</span></span>
<span data-ttu-id="342f3-103">Állítsa le a Kubectl SSH-alagutat a Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="342f3-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="342f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="342f3-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="342f3-105">DESCRIPTION</span></span>
<span data-ttu-id="342f3-106">Állítsa le a Kubectl SSH-alagutat a Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="342f3-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="342f3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="342f3-107">EXAMPLES</span></span>

### <span data-ttu-id="342f3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="342f3-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="342f3-109">A meglévő SSH bújtatási beállítás leállítása a Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="342f3-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="342f3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="342f3-110">PARAMETERS</span></span>

### <span data-ttu-id="342f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342f3-111">-DefaultProfile</span></span>
<span data-ttu-id="342f3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="342f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342f3-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="342f3-113">-PassThru</span></span>
<span data-ttu-id="342f3-114">Igaz értéket ad eredményül, ha az SSH bújtatás be van zárva.</span><span class="sxs-lookup"><span data-stu-id="342f3-114">Returns true if SSH tunnel is closed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342f3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342f3-115">CommonParameters</span></span>
<span data-ttu-id="342f3-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="342f3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342f3-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="342f3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342f3-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="342f3-118">INPUTS</span></span>

### <span data-ttu-id="342f3-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="342f3-119">None</span></span>

## <span data-ttu-id="342f3-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="342f3-120">OUTPUTS</span></span>

### <span data-ttu-id="342f3-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="342f3-121">System.Boolean</span></span>

## <span data-ttu-id="342f3-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="342f3-122">NOTES</span></span>

## <span data-ttu-id="342f3-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="342f3-123">RELATED LINKS</span></span>
