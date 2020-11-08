---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182457"
---
# <span data-ttu-id="24a1c-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="24a1c-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="24a1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="24a1c-103">Get-AzWebAppContainerContinuousDeploymentUrl a tároló folyamatos telepítő URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="24a1c-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="24a1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a1c-104">SYNTAX</span></span>

### <span data-ttu-id="24a1c-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24a1c-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a1c-106">S2</span><span class="sxs-lookup"><span data-stu-id="24a1c-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24a1c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a1c-107">DESCRIPTION</span></span>
<span data-ttu-id="24a1c-108">Get-AzWebAppContainerContinuousDeploymentUrl a tároló folyamatos telepítő URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="24a1c-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="24a1c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="24a1c-109">EXAMPLES</span></span>

### <span data-ttu-id="24a1c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24a1c-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="24a1c-111">Ez a parancs a tároló folyamatos telepítő URL-címét fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="24a1c-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="24a1c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a1c-112">PARAMETERS</span></span>

### <span data-ttu-id="24a1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a1c-113">-DefaultProfile</span></span>
<span data-ttu-id="24a1c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a1c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a1c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24a1c-115">-Name</span></span>
<span data-ttu-id="24a1c-116">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="24a1c-116">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="24a1c-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24a1c-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a1c-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="24a1c-119">-SlotName</span></span>
<span data-ttu-id="24a1c-120">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="24a1c-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a1c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="24a1c-121">-WebApp</span></span>
<span data-ttu-id="24a1c-122">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="24a1c-122">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24a1c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a1c-123">CommonParameters</span></span>
<span data-ttu-id="24a1c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a1c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a1c-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a1c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a1c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a1c-126">INPUTS</span></span>

### <span data-ttu-id="24a1c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1c-127">System.String</span></span>

### <span data-ttu-id="24a1c-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="24a1c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="24a1c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a1c-129">OUTPUTS</span></span>

### <span data-ttu-id="24a1c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1c-130">System.String</span></span>

## <span data-ttu-id="24a1c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a1c-131">NOTES</span></span>

## <span data-ttu-id="24a1c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a1c-132">RELATED LINKS</span></span>
