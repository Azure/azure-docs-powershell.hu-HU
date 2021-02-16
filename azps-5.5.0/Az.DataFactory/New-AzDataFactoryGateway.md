---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: a4c755ab3f68eab2821807e7df6b9e24fad0df9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163810"
---
# <span data-ttu-id="b49d5-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b49d5-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="b49d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b49d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b49d5-103">Átjárót hoz létre egy Azure Data Factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="b49d5-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="b49d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b49d5-104">SYNTAX</span></span>

### <span data-ttu-id="b49d5-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b49d5-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b49d5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b49d5-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b49d5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b49d5-107">DESCRIPTION</span></span>
<span data-ttu-id="b49d5-108">A **New-AzDataFactoryGateway** parancsmag létrehoz egy átjárót az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="b49d5-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="b49d5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b49d5-109">EXAMPLES</span></span>

### <span data-ttu-id="b49d5-110">1. példa: Átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="b49d5-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="b49d5-111">Ez a parancs létrehoz egy ContosoGateway nevű átjárót a WikiADF nevű adatüzemben az ADF nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="b49d5-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="b49d5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b49d5-112">PARAMETERS</span></span>

### <span data-ttu-id="b49d5-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b49d5-113">-DataFactory</span></span>
<span data-ttu-id="b49d5-114">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b49d5-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b49d5-115">Ez a parancsmag létrehoz egy átjárót a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="b49d5-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49d5-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b49d5-116">-DataFactoryName</span></span>
<span data-ttu-id="b49d5-117">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b49d5-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b49d5-118">Ez a parancsmag létrehoz egy átjárót a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="b49d5-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49d5-119">-DefaultProfile</span></span>
<span data-ttu-id="b49d5-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b49d5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b49d5-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b49d5-121">-Description</span></span>
<span data-ttu-id="b49d5-122">Megadja az átjáró leírását.</span><span class="sxs-lookup"><span data-stu-id="b49d5-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49d5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b49d5-123">-Name</span></span>
<span data-ttu-id="b49d5-124">A létrehozni használt átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b49d5-124">Specifies the name of the gateway to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="b49d5-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b49d5-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b49d5-127">Ez a parancsmag létrehoz egy átjárót, amely a paraméter által megadott csoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="b49d5-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49d5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49d5-128">CommonParameters</span></span>
<span data-ttu-id="b49d5-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49d5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49d5-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49d5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49d5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b49d5-131">INPUTS</span></span>

### <span data-ttu-id="b49d5-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b49d5-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b49d5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b49d5-133">System.String</span></span>

## <span data-ttu-id="b49d5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b49d5-134">OUTPUTS</span></span>

### <span data-ttu-id="b49d5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b49d5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="b49d5-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b49d5-136">NOTES</span></span>
* <span data-ttu-id="b49d5-137">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="b49d5-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b49d5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b49d5-138">RELATED LINKS</span></span>

[<span data-ttu-id="b49d5-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b49d5-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="b49d5-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b49d5-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


