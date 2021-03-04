---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 191b5a75a5f9f581308c8d5aa214fe4f2ae84851
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936865"
---
# <span data-ttu-id="a8d11-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="a8d11-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="a8d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d11-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d11-103">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="a8d11-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="a8d11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8d11-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8d11-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8d11-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d11-106">Információkat kap az IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="a8d11-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="a8d11-107">Az IotHub-feladat akkor jön létre, amikor importálási vagy exportálási művelet inicializálódik a New-AzIotHubExportDevices vagy New-AzIotHubImportDevices paranccsal.</span><span class="sxs-lookup"><span data-stu-id="a8d11-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="a8d11-108">Felsorolhatja az összes feladatot, vagy szűrheti őket a feladatazonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="a8d11-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="a8d11-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8d11-109">EXAMPLES</span></span>

### <span data-ttu-id="a8d11-110">1. példa az összes feladat felsorolásához</span><span class="sxs-lookup"><span data-stu-id="a8d11-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a8d11-111">A myiothub nevű IotHub összes állását átveszi</span><span class="sxs-lookup"><span data-stu-id="a8d11-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="a8d11-112">2. példa: Adott feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="a8d11-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="a8d11-113">Információkat kap a feladatról a "myiothub" nevű IotHub "3630fc31-4caa-43e8-a232-ea0577221cb2" azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a8d11-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a8d11-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8d11-114">PARAMETERS</span></span>

### <span data-ttu-id="a8d11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d11-115">-DefaultProfile</span></span>
<span data-ttu-id="a8d11-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8d11-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8d11-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="a8d11-117">-JobId</span></span>
<span data-ttu-id="a8d11-118">A feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a8d11-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8d11-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a8d11-119">-Name</span></span>
<span data-ttu-id="a8d11-120">Az IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="a8d11-120">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d11-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8d11-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a8d11-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d11-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d11-123">CommonParameters</span></span>
<span data-ttu-id="a8d11-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d11-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d11-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8d11-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d11-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8d11-126">INPUTS</span></span>

### <span data-ttu-id="a8d11-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a8d11-127">System.String</span></span>

## <span data-ttu-id="a8d11-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8d11-128">OUTPUTS</span></span>

### <span data-ttu-id="a8d11-129">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubFeladatResponse</span><span class="sxs-lookup"><span data-stu-id="a8d11-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a8d11-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8d11-130">NOTES</span></span>

## <span data-ttu-id="a8d11-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8d11-131">RELATED LINKS</span></span>
