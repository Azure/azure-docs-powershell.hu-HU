---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495572"
---
# <span data-ttu-id="4ad83-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="4ad83-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="4ad83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ad83-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad83-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl a tároló folyamatos telepítő URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="4ad83-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ad83-104">SYNTAX</span></span>

### <span data-ttu-id="4ad83-105">S1</span><span class="sxs-lookup"><span data-stu-id="4ad83-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ad83-106">S2</span><span class="sxs-lookup"><span data-stu-id="4ad83-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ad83-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ad83-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad83-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl a tároló folyamatos telepítő URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="4ad83-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="4ad83-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4ad83-109">EXAMPLES</span></span>

### <span data-ttu-id="4ad83-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ad83-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="4ad83-111">Ez a parancs a tároló folyamatos telepítő URL-címét fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="4ad83-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="4ad83-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ad83-112">PARAMETERS</span></span>

### <span data-ttu-id="4ad83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad83-113">-DefaultProfile</span></span>
<span data-ttu-id="4ad83-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ad83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad83-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ad83-115">-Name</span></span>
<span data-ttu-id="4ad83-116">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="4ad83-116">The name of the web app.</span></span>

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

### <span data-ttu-id="4ad83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad83-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ad83-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4ad83-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ad83-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="4ad83-119">-SlotName</span></span>
<span data-ttu-id="4ad83-120">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="4ad83-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="4ad83-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4ad83-121">-WebApp</span></span>
<span data-ttu-id="4ad83-122">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="4ad83-122">The web app object</span></span>

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

### <span data-ttu-id="4ad83-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad83-123">CommonParameters</span></span>
<span data-ttu-id="4ad83-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ad83-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad83-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad83-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad83-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad83-126">INPUTS</span></span>

### <span data-ttu-id="4ad83-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4ad83-127">System.String</span></span>
### <span data-ttu-id="4ad83-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="4ad83-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="4ad83-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad83-129">OUTPUTS</span></span>

### <span data-ttu-id="4ad83-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4ad83-130">System.String</span></span>
## <span data-ttu-id="4ad83-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ad83-131">NOTES</span></span>

## <span data-ttu-id="4ad83-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ad83-132">RELATED LINKS</span></span>
