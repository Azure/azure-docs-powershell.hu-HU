---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185050"
---
# <span data-ttu-id="8c38a-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="8c38a-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="8c38a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c38a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c38a-103">Egy önállóan működtetett integrációs futásidejű kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="8c38a-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="8c38a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c38a-104">SYNTAX</span></span>

### <span data-ttu-id="8c38a-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c38a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c38a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c38a-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c38a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8c38a-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c38a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c38a-108">DESCRIPTION</span></span>
<span data-ttu-id="8c38a-109">Beolvashatja az integrációs futtatókörnyezet kulcsait.</span><span class="sxs-lookup"><span data-stu-id="8c38a-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="8c38a-110">A kulcsok az integrációs futásidejű csomópontok regisztrálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="8c38a-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="8c38a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8c38a-111">EXAMPLES</span></span>

### <span data-ttu-id="8c38a-112">Példa 1: integrációs futásidejű kulcsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="8c38a-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="8c38a-113">A parancsmag a ' teszt-selfhost-IR ' nevű integrációs futásidejű kulcsait keresi meg.</span><span class="sxs-lookup"><span data-stu-id="8c38a-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="8c38a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c38a-114">PARAMETERS</span></span>

### <span data-ttu-id="8c38a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8c38a-115">-DataFactoryName</span></span>
<span data-ttu-id="8c38a-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="8c38a-116">The data factory name.</span></span>

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

### <span data-ttu-id="8c38a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c38a-117">-DefaultProfile</span></span>
<span data-ttu-id="8c38a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c38a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c38a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c38a-119">-InputObject</span></span>
<span data-ttu-id="8c38a-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="8c38a-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="8c38a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c38a-121">-Name</span></span>
<span data-ttu-id="8c38a-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="8c38a-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="8c38a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c38a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c38a-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c38a-124">The resource group name.</span></span>

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

### <span data-ttu-id="8c38a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c38a-125">-ResourceId</span></span>
<span data-ttu-id="8c38a-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8c38a-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8c38a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c38a-127">CommonParameters</span></span>
<span data-ttu-id="8c38a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c38a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c38a-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c38a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c38a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c38a-130">INPUTS</span></span>

### <span data-ttu-id="8c38a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8c38a-131">System.String</span></span>

### <span data-ttu-id="8c38a-132">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8c38a-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8c38a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c38a-133">OUTPUTS</span></span>

### <span data-ttu-id="8c38a-134">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="8c38a-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="8c38a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c38a-135">NOTES</span></span>

## <span data-ttu-id="8c38a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c38a-136">RELATED LINKS</span></span>

[<span data-ttu-id="8c38a-137">Új – AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="8c38a-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
