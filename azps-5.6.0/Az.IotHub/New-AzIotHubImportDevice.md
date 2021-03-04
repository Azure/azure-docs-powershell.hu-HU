---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: f2a2daebcb77746ae087fe527245376963fade5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920690"
---
# <span data-ttu-id="f89f0-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="f89f0-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="f89f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f89f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f89f0-103">Létrehoz egy új importálási eszköz-feladatot.</span><span class="sxs-lookup"><span data-stu-id="f89f0-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="f89f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f89f0-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f89f0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f89f0-105">DESCRIPTION</span></span>
<span data-ttu-id="f89f0-106">Új importálási eszköz feladatot hoz létre az IotHubhoz.</span><span class="sxs-lookup"><span data-stu-id="f89f0-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="f89f0-107">Ezzel az összes eszközt importálja az IotHubra a megadott tárolóból.</span><span class="sxs-lookup"><span data-stu-id="f89f0-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="f89f0-108">Az SAS URI létrehozásáról az alábbi cikkben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f89f0-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="f89f0-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="f89f0-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="f89f0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f89f0-110">EXAMPLES</span></span>

### <span data-ttu-id="f89f0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f89f0-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="f89f0-112">Létrehoz egy új importálási eszközkérést az IotHub "myiothub" számára.</span><span class="sxs-lookup"><span data-stu-id="f89f0-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="f89f0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f89f0-113">PARAMETERS</span></span>

### <span data-ttu-id="f89f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89f0-114">-DefaultProfile</span></span>
<span data-ttu-id="f89f0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f89f0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f89f0-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f89f0-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="f89f0-117">Input Blob Container Uri for FileUpload</span><span class="sxs-lookup"><span data-stu-id="f89f0-117">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f89f0-118">-Name</span></span>
<span data-ttu-id="f89f0-119">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="f89f0-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="f89f0-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f89f0-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="f89f0-121">Az Uri, amelybe a kimenetet írni kell.</span><span class="sxs-lookup"><span data-stu-id="f89f0-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f89f0-122">-ResourceGroupName</span></span>
<span data-ttu-id="f89f0-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f89f0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f89f0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f89f0-124">-Confirm</span></span>
<span data-ttu-id="f89f0-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f89f0-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f89f0-126">-WhatIf</span></span>
<span data-ttu-id="f89f0-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f89f0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f89f0-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f89f0-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89f0-129">CommonParameters</span></span>
<span data-ttu-id="f89f0-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f89f0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89f0-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89f0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89f0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f89f0-132">INPUTS</span></span>

### <span data-ttu-id="f89f0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f89f0-133">System.String</span></span>

## <span data-ttu-id="f89f0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f89f0-134">OUTPUTS</span></span>

### <span data-ttu-id="f89f0-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubFeladatResponse</span><span class="sxs-lookup"><span data-stu-id="f89f0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="f89f0-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f89f0-136">NOTES</span></span>

## <span data-ttu-id="f89f0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f89f0-137">RELATED LINKS</span></span>
