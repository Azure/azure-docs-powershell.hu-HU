---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2a1aaef2532e8c0a00a04a42d857e2be0e2a0451
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836533"
---
# <span data-ttu-id="d81fb-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d81fb-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="d81fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d81fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d81fb-103">Egy önállóan működtetett integrációs futásidejű kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="d81fb-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="d81fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d81fb-104">SYNTAX</span></span>

### <span data-ttu-id="d81fb-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d81fb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d81fb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d81fb-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d81fb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d81fb-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d81fb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d81fb-108">DESCRIPTION</span></span>
<span data-ttu-id="d81fb-109">Beolvashatja az integrációs futtatókörnyezet kulcsait.</span><span class="sxs-lookup"><span data-stu-id="d81fb-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="d81fb-110">A kulcsok az integrációs futásidejű csomópontok regisztrálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="d81fb-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="d81fb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d81fb-111">EXAMPLES</span></span>

### <span data-ttu-id="d81fb-112">Példa 1: integrációs futásidejű kulcsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="d81fb-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="d81fb-113">A parancsmag a ' teszt-selfhost-IR ' nevű integrációs futásidejű kulcsait keresi meg.</span><span class="sxs-lookup"><span data-stu-id="d81fb-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d81fb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d81fb-114">PARAMETERS</span></span>

### <span data-ttu-id="d81fb-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d81fb-115">-DataFactoryName</span></span>
<span data-ttu-id="d81fb-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="d81fb-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d81fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81fb-117">-DefaultProfile</span></span>
<span data-ttu-id="d81fb-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d81fb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d81fb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d81fb-119">-InputObject</span></span>
<span data-ttu-id="d81fb-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="d81fb-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d81fb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d81fb-121">-Name</span></span>
<span data-ttu-id="d81fb-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="d81fb-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d81fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="d81fb-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d81fb-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d81fb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d81fb-125">-ResourceId</span></span>
<span data-ttu-id="d81fb-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d81fb-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d81fb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81fb-127">CommonParameters</span></span>
<span data-ttu-id="d81fb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d81fb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81fb-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d81fb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81fb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d81fb-130">INPUTS</span></span>

### <span data-ttu-id="d81fb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d81fb-131">System.String</span></span>

### <span data-ttu-id="d81fb-132">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d81fb-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d81fb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d81fb-133">OUTPUTS</span></span>

### <span data-ttu-id="d81fb-134">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="d81fb-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="d81fb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d81fb-135">NOTES</span></span>

## <span data-ttu-id="d81fb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d81fb-136">RELATED LINKS</span></span>

[<span data-ttu-id="d81fb-137">Új – AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d81fb-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
