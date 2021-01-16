---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335525"
---
# <span data-ttu-id="451a9-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="451a9-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="451a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="451a9-102">SYNOPSIS</span></span>
<span data-ttu-id="451a9-103">Beállítja egy átjáró leírását az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="451a9-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="451a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="451a9-104">SYNTAX</span></span>

### <span data-ttu-id="451a9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="451a9-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="451a9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="451a9-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="451a9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="451a9-107">DESCRIPTION</span></span>
<span data-ttu-id="451a9-108">A **Set-AzDataFactoryGateway** parancsmag beállítja a megadott átjáró leírását az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="451a9-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="451a9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="451a9-109">EXAMPLES</span></span>

### <span data-ttu-id="451a9-110">1. példa: Átjáró leírásának beállítása</span><span class="sxs-lookup"><span data-stu-id="451a9-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="451a9-111">Ez a parancs beállítja a ContosoGateway nevű átjáró leírását a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="451a9-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="451a9-112">A Leírás paraméter az új leírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="451a9-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="451a9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="451a9-113">PARAMETERS</span></span>

### <span data-ttu-id="451a9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="451a9-114">-DataFactory</span></span>
<span data-ttu-id="451a9-115">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="451a9-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="451a9-116">Ez a parancsmag beállítja az átjáró leírását a paraméter által megadott adathalmazban.</span><span class="sxs-lookup"><span data-stu-id="451a9-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="451a9-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="451a9-117">-DataFactoryName</span></span>
<span data-ttu-id="451a9-118">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="451a9-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="451a9-119">Ez a parancsmag beállítja az átjáró leírását a paraméter által megadott adathalmazban.</span><span class="sxs-lookup"><span data-stu-id="451a9-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="451a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451a9-120">-DefaultProfile</span></span>
<span data-ttu-id="451a9-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="451a9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="451a9-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="451a9-122">-Description</span></span>
<span data-ttu-id="451a9-123">Megadja az átjáró leírását.</span><span class="sxs-lookup"><span data-stu-id="451a9-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="451a9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="451a9-124">-Name</span></span>
<span data-ttu-id="451a9-125">Annak az átjárónak a nevét adja meg, amelyhez leírást kell beállítani.</span><span class="sxs-lookup"><span data-stu-id="451a9-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="451a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="451a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="451a9-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="451a9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="451a9-128">Ez a parancsmag beállítja a paraméter által megadott csoporthoz tartozó átjáró leírását.</span><span class="sxs-lookup"><span data-stu-id="451a9-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="451a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451a9-129">CommonParameters</span></span>
<span data-ttu-id="451a9-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="451a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451a9-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="451a9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451a9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="451a9-132">INPUTS</span></span>

### <span data-ttu-id="451a9-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="451a9-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="451a9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="451a9-134">System.String</span></span>

## <span data-ttu-id="451a9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="451a9-135">OUTPUTS</span></span>

### <span data-ttu-id="451a9-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="451a9-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="451a9-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="451a9-137">NOTES</span></span>
* <span data-ttu-id="451a9-138">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="451a9-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="451a9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="451a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="451a9-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="451a9-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="451a9-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="451a9-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="451a9-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="451a9-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


