---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480415"
---
# <span data-ttu-id="762b4-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="762b4-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="762b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="762b4-102">SYNOPSIS</span></span>
<span data-ttu-id="762b4-103">Hitelesítéskulcsot hoz létre egy Azure Data Factory-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="762b4-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="762b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="762b4-104">SYNTAX</span></span>

### <span data-ttu-id="762b4-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="762b4-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="762b4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="762b4-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="762b4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="762b4-107">DESCRIPTION</span></span>
<span data-ttu-id="762b4-108">A **New-AzDataFactoryGatewayAuthKey** parancsmag átjáró-hitelesítéskulcsot hoz létre egy megadott Azure Data Factory-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="762b4-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="762b4-109">Ezzel a kulccsal regisztrálhatja az átjárót egy felhőszolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="762b4-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="762b4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="762b4-110">EXAMPLES</span></span>

### <span data-ttu-id="762b4-111">1. példa: Átjárói hitelesítéskulcs létrehozása a Key1 kulcshoz</span><span class="sxs-lookup"><span data-stu-id="762b4-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="762b4-112">Ez a parancs létrehozza a Key1 kulcs egy átjáró-hitelesítési kulcsát a MyGateway nevű adat gyári átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="762b4-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="762b4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="762b4-113">PARAMETERS</span></span>

### <span data-ttu-id="762b4-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="762b4-114">-DataFactoryName</span></span>
<span data-ttu-id="762b4-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="762b4-115">The data factory name.</span></span>

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

### <span data-ttu-id="762b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762b4-116">-DefaultProfile</span></span>
<span data-ttu-id="762b4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="762b4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="762b4-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="762b4-118">-GatewayName</span></span>
<span data-ttu-id="762b4-119">Az adatüzemi átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="762b4-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="762b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="762b4-120">-InputObject</span></span>
<span data-ttu-id="762b4-121">The data factory object</span><span class="sxs-lookup"><span data-stu-id="762b4-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="762b4-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="762b4-122">-KeyName</span></span>
<span data-ttu-id="762b4-123">Az újragenerálható átjáró-hitelesítési kulcs neve , "kulcs1" vagy "kulcs2".</span><span class="sxs-lookup"><span data-stu-id="762b4-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="762b4-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="762b4-125">The resource group name.</span></span>

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

### <span data-ttu-id="762b4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="762b4-126">-Confirm</span></span>
<span data-ttu-id="762b4-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="762b4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762b4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762b4-128">-WhatIf</span></span>
<span data-ttu-id="762b4-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="762b4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="762b4-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="762b4-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762b4-131">CommonParameters</span></span>
<span data-ttu-id="762b4-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762b4-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762b4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762b4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="762b4-134">INPUTS</span></span>

### <span data-ttu-id="762b4-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="762b4-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="762b4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="762b4-136">System.String</span></span>

## <span data-ttu-id="762b4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="762b4-137">OUTPUTS</span></span>

### <span data-ttu-id="762b4-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="762b4-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="762b4-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="762b4-139">NOTES</span></span>
* <span data-ttu-id="762b4-140">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="762b4-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="762b4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="762b4-141">RELATED LINKS</span></span>

<span data-ttu-id="762b4-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="762b4-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

