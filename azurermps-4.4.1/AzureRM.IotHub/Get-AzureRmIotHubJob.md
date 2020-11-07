---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: b0ea6f3cae3fe978a3d24b055eb47693ea466272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679436"
---
# <span data-ttu-id="8f26e-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="8f26e-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="8f26e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f26e-102">SYNOPSIS</span></span>
<span data-ttu-id="8f26e-103">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="8f26e-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f26e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f26e-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f26e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f26e-105">DESCRIPTION</span></span>
<span data-ttu-id="8f26e-106">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="8f26e-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="8f26e-107">Az IotHub-feladat akkor jön létre, ha az importálási vagy exportálási műveletet az New-AzureRmIotHubExportDevices vagy a New-AzureRmIotHubImportDevices parancs segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="8f26e-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="8f26e-108">A projekt azonosítóval listázhatja az összes feladatot, vagy szűrheti a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="8f26e-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="8f26e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8f26e-109">EXAMPLES</span></span>

### <span data-ttu-id="8f26e-110">Példa 1 minden feladat listázása</span><span class="sxs-lookup"><span data-stu-id="8f26e-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8f26e-111">A "myiothub" nevű IotHub minden feladatát kapja</span><span class="sxs-lookup"><span data-stu-id="8f26e-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="8f26e-112">Példa 2 adott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="8f26e-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="8f26e-113">Információt kap a feladatról a "3630fc31-4caa-43e8-A232-ea0577221cb2" azonosítóval az "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="8f26e-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8f26e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f26e-114">PARAMETERS</span></span>

### <span data-ttu-id="8f26e-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="8f26e-115">-JobId</span></span>
<span data-ttu-id="8f26e-116">A projekt azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8f26e-116">The Job Identifier.</span></span> 

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

### <span data-ttu-id="8f26e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f26e-117">-Name</span></span>
<span data-ttu-id="8f26e-118">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="8f26e-118">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="8f26e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f26e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f26e-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8f26e-120">Resource Group Name</span></span>

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

### <span data-ttu-id="8f26e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f26e-121">-DefaultProfile</span></span>
<span data-ttu-id="8f26e-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f26e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f26e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f26e-123">CommonParameters</span></span>
<span data-ttu-id="8f26e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f26e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f26e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f26e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f26e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f26e-126">INPUTS</span></span>

### <span data-ttu-id="8f26e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8f26e-127">System.String</span></span>

## <span data-ttu-id="8f26e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f26e-128">OUTPUTS</span></span>

### <span data-ttu-id="8f26e-129">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="8f26e-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="8f26e-130">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="8f26e-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="8f26e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f26e-131">NOTES</span></span>

## <span data-ttu-id="8f26e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f26e-132">RELATED LINKS</span></span>

