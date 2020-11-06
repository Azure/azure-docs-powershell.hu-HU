---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: eb248e1059da6dcab581e4fba8b3eac7f970bb30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497624"
---
# <span data-ttu-id="0928f-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0928f-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="0928f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0928f-102">SYNOPSIS</span></span>
<span data-ttu-id="0928f-103">Egy önállóan működtetett integrációs futásidejű kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="0928f-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0928f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0928f-104">SYNTAX</span></span>

### <span data-ttu-id="0928f-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0928f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0928f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0928f-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0928f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0928f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0928f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0928f-108">DESCRIPTION</span></span>
<span data-ttu-id="0928f-109">Beolvashatja az integrációs futtatókörnyezet kulcsait.</span><span class="sxs-lookup"><span data-stu-id="0928f-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="0928f-110">A kulcsok az integrációs futásidejű csomópontok regisztrálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="0928f-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="0928f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0928f-111">EXAMPLES</span></span>

### <span data-ttu-id="0928f-112">Példa 1: integrációs futásidejű kulcsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="0928f-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="0928f-113">A parancsmag a ' teszt-selfhost-IR ' nevű integrációs futásidejű kulcsait keresi meg.</span><span class="sxs-lookup"><span data-stu-id="0928f-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0928f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0928f-114">PARAMETERS</span></span>

### <span data-ttu-id="0928f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0928f-115">-DataFactoryName</span></span>
<span data-ttu-id="0928f-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0928f-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0928f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0928f-117">-DefaultProfile</span></span>
<span data-ttu-id="0928f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0928f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0928f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0928f-119">-InputObject</span></span>
<span data-ttu-id="0928f-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="0928f-120">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0928f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0928f-121">-Name</span></span>
<span data-ttu-id="0928f-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="0928f-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0928f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0928f-123">-ResourceGroupName</span></span>
<span data-ttu-id="0928f-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0928f-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0928f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0928f-125">-ResourceId</span></span>
<span data-ttu-id="0928f-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0928f-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0928f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0928f-127">CommonParameters</span></span>
<span data-ttu-id="0928f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0928f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0928f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0928f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0928f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0928f-130">INPUTS</span></span>

### <span data-ttu-id="0928f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0928f-131">System.String</span></span>
<span data-ttu-id="0928f-132">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0928f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="0928f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0928f-133">OUTPUTS</span></span>

### <span data-ttu-id="0928f-134">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="0928f-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="0928f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0928f-135">NOTES</span></span>

## <span data-ttu-id="0928f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0928f-136">RELATED LINKS</span></span>

[<span data-ttu-id="0928f-137">Új – AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0928f-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
