---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 19d4022fcf5f3eee0ee8d77e7c061ae2f8d00629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504203"
---
# <span data-ttu-id="eba71-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="eba71-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="eba71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eba71-102">SYNOPSIS</span></span>
<span data-ttu-id="eba71-103">SQL Server-bővítmény eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="eba71-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eba71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eba71-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eba71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eba71-105">DESCRIPTION</span></span>
<span data-ttu-id="eba71-106">A **Remove-AzureRmVMSqlServerExtension** parancsmag eltávolítja a AzureSQL Server-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="eba71-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="eba71-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eba71-107">EXAMPLES</span></span>

### <span data-ttu-id="eba71-108">1. példa: SQL Server-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="eba71-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="eba71-109">Ez a parancs eltávolítja az SQL Server-bővítményt a ContosoVM22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="eba71-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="eba71-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eba71-110">PARAMETERS</span></span>

### <span data-ttu-id="eba71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba71-111">-DefaultProfile</span></span>
<span data-ttu-id="eba71-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eba71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eba71-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eba71-113">-Name</span></span>
<span data-ttu-id="eba71-114">Annak az SQL-kiszolgálónak a neve, amely a parancsmag által eltávolított bővítmény.</span><span class="sxs-lookup"><span data-stu-id="eba71-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba71-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba71-115">-ResourceGroupName</span></span>
<span data-ttu-id="eba71-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eba71-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eba71-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="eba71-117">-VMName</span></span>
<span data-ttu-id="eba71-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="eba71-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba71-119">CommonParameters</span></span>
<span data-ttu-id="eba71-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eba71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba71-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba71-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba71-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eba71-122">INPUTS</span></span>

## <span data-ttu-id="eba71-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eba71-123">OUTPUTS</span></span>

## <span data-ttu-id="eba71-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eba71-124">NOTES</span></span>

## <span data-ttu-id="eba71-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eba71-125">RELATED LINKS</span></span>

[<span data-ttu-id="eba71-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="eba71-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="eba71-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="eba71-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


