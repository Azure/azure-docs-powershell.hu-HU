---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: bb1b5579869c7142bcf6cbe168ff10aaa9b7e083
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147762"
---
# <span data-ttu-id="c2b38-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="c2b38-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="c2b38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b38-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b38-103">Létrehoz egy új importálási eszköz-feladatot.</span><span class="sxs-lookup"><span data-stu-id="c2b38-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="c2b38-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2b38-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2b38-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2b38-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b38-106">Új importálási eszköz feladatot hoz létre az IotHubhoz.</span><span class="sxs-lookup"><span data-stu-id="c2b38-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="c2b38-107">Ezzel az összes eszközt importálja az IotHubra a megadott tárolóból.</span><span class="sxs-lookup"><span data-stu-id="c2b38-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="c2b38-108">Az SAS URI létrehozásáról az alábbi cikkben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c2b38-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="c2b38-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="c2b38-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="c2b38-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2b38-110">EXAMPLES</span></span>

### <span data-ttu-id="c2b38-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2b38-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="c2b38-112">Létrehoz egy új importálási eszközkérést az IotHub "myiothub" számára.</span><span class="sxs-lookup"><span data-stu-id="c2b38-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="c2b38-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2b38-113">PARAMETERS</span></span>

### <span data-ttu-id="c2b38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b38-114">-DefaultProfile</span></span>
<span data-ttu-id="c2b38-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c2b38-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2b38-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="c2b38-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="c2b38-117">Input Blob Container Uri for FileUpload</span><span class="sxs-lookup"><span data-stu-id="c2b38-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="c2b38-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c2b38-118">-Name</span></span>
<span data-ttu-id="c2b38-119">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="c2b38-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="c2b38-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="c2b38-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="c2b38-121">Az Uri, amelybe a kimenetet írni kell.</span><span class="sxs-lookup"><span data-stu-id="c2b38-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="c2b38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b38-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2b38-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c2b38-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c2b38-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2b38-124">-Confirm</span></span>
<span data-ttu-id="c2b38-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c2b38-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b38-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b38-126">-WhatIf</span></span>
<span data-ttu-id="c2b38-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c2b38-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b38-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2b38-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b38-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b38-129">CommonParameters</span></span>
<span data-ttu-id="c2b38-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b38-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b38-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b38-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b38-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2b38-132">INPUTS</span></span>

### <span data-ttu-id="c2b38-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c2b38-133">System.String</span></span>

## <span data-ttu-id="c2b38-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2b38-134">OUTPUTS</span></span>

### <span data-ttu-id="c2b38-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubFeladatResponse</span><span class="sxs-lookup"><span data-stu-id="c2b38-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="c2b38-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2b38-136">NOTES</span></span>

## <span data-ttu-id="c2b38-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2b38-137">RELATED LINKS</span></span>
