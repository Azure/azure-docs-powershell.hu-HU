---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: ed7ad2edb0c82203f571edccf9b6672428956ac2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839977"
---
# <span data-ttu-id="c9ed8-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="c9ed8-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="c9ed8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ed8-103">Get-AzWebAppContainerContinuousDeploymentUrl a tároló folyamatos telepítő URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="c9ed8-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="c9ed8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9ed8-104">SYNTAX</span></span>

### <span data-ttu-id="c9ed8-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9ed8-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9ed8-106">S2</span><span class="sxs-lookup"><span data-stu-id="c9ed8-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9ed8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="c9ed8-108">Get-AzWebAppContainerContinuousDeploymentUrl a tároló folyamatos telepítő URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="c9ed8-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="c9ed8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c9ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="c9ed8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9ed8-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="c9ed8-111">Ez a parancs a tároló folyamatos telepítő URL-címét fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="c9ed8-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="c9ed8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9ed8-112">PARAMETERS</span></span>

### <span data-ttu-id="c9ed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ed8-113">-DefaultProfile</span></span>
<span data-ttu-id="c9ed8-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9ed8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9ed8-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9ed8-115">-Name</span></span>
<span data-ttu-id="c9ed8-116">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="c9ed8-116">The name of the web app.</span></span>

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

### <span data-ttu-id="c9ed8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ed8-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9ed8-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9ed8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9ed8-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="c9ed8-119">-SlotName</span></span>
<span data-ttu-id="c9ed8-120">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="c9ed8-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="c9ed8-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c9ed8-121">-WebApp</span></span>
<span data-ttu-id="c9ed8-122">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="c9ed8-122">The web app object</span></span>

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

### <span data-ttu-id="c9ed8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ed8-123">CommonParameters</span></span>
<span data-ttu-id="c9ed8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9ed8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ed8-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ed8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ed8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9ed8-126">INPUTS</span></span>

### <span data-ttu-id="c9ed8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c9ed8-127">System.String</span></span>

### <span data-ttu-id="c9ed8-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c9ed8-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9ed8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9ed8-129">OUTPUTS</span></span>

### <span data-ttu-id="c9ed8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c9ed8-130">System.String</span></span>

## <span data-ttu-id="c9ed8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9ed8-131">NOTES</span></span>

## <span data-ttu-id="c9ed8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9ed8-132">RELATED LINKS</span></span>
