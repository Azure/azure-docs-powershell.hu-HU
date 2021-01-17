---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480432"
---
# <span data-ttu-id="ececf-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ececf-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="ececf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ececf-102">SYNOPSIS</span></span>
<span data-ttu-id="ececf-103">Leküldi az önkiszolgáló integrációs futásidejű billentyűparancsokat.</span><span class="sxs-lookup"><span data-stu-id="ececf-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="ececf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ececf-104">SYNTAX</span></span>

### <span data-ttu-id="ececf-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ececf-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ececf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ececf-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ececf-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ececf-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ececf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ececf-108">DESCRIPTION</span></span>
<span data-ttu-id="ececf-109">Az integrációs futásidejű billentyűparancsok lekérte.</span><span class="sxs-lookup"><span data-stu-id="ececf-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="ececf-110">A kulcsok egy integrációs futásidejű csomópont regisztrálását használják.</span><span class="sxs-lookup"><span data-stu-id="ececf-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="ececf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ececf-111">EXAMPLES</span></span>

### <span data-ttu-id="ececf-112">1. példa: Integrációs futásidejű kulcsok lekérte</span><span class="sxs-lookup"><span data-stu-id="ececf-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="ececf-113">A parancsmag lekéri a "test-selfhost-ir" nevű integrációs futási idő kulcsait.</span><span class="sxs-lookup"><span data-stu-id="ececf-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ececf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ececf-114">PARAMETERS</span></span>

### <span data-ttu-id="ececf-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ececf-115">-DataFactoryName</span></span>
<span data-ttu-id="ececf-116">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="ececf-116">The data factory name.</span></span>

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

### <span data-ttu-id="ececf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ececf-117">-DefaultProfile</span></span>
<span data-ttu-id="ececf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ececf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ececf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ececf-119">-InputObject</span></span>
<span data-ttu-id="ececf-120">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="ececf-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="ececf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ececf-121">-Name</span></span>
<span data-ttu-id="ececf-122">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="ececf-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="ececf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ececf-123">-ResourceGroupName</span></span>
<span data-ttu-id="ececf-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ececf-124">The resource group name.</span></span>

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

### <span data-ttu-id="ececf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ececf-125">-ResourceId</span></span>
<span data-ttu-id="ececf-126">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="ececf-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ececf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ececf-127">CommonParameters</span></span>
<span data-ttu-id="ececf-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ececf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ececf-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ececf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ececf-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ececf-130">INPUTS</span></span>

### <span data-ttu-id="ececf-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ececf-131">System.String</span></span>

### <span data-ttu-id="ececf-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ececf-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ececf-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ececf-133">OUTPUTS</span></span>

### <span data-ttu-id="ececf-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="ececf-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="ececf-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ececf-135">NOTES</span></span>

## <span data-ttu-id="ececf-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ececf-136">RELATED LINKS</span></span>

[<span data-ttu-id="ececf-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ececf-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
