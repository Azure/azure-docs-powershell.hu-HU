---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671274"
---
# <span data-ttu-id="f2fab-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f2fab-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="f2fab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2fab-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fab-103">SQL Server-bővítmény eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="f2fab-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="f2fab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2fab-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2fab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2fab-105">DESCRIPTION</span></span>
<span data-ttu-id="f2fab-106">A **Remove-AzVMSqlServerExtension** parancsmag eltávolítja a AzureSQL Server-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="f2fab-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="f2fab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f2fab-107">EXAMPLES</span></span>

### <span data-ttu-id="f2fab-108">1. példa: SQL Server-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f2fab-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="f2fab-109">Ez a parancs eltávolítja az SQL Server-bővítményt a ContosoVM22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="f2fab-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="f2fab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2fab-110">PARAMETERS</span></span>

### <span data-ttu-id="f2fab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fab-111">-DefaultProfile</span></span>
<span data-ttu-id="f2fab-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2fab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2fab-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2fab-113">-Name</span></span>
<span data-ttu-id="f2fab-114">Annak az SQL-kiszolgálónak a neve, amely a parancsmag által eltávolított bővítmény.</span><span class="sxs-lookup"><span data-stu-id="f2fab-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f2fab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2fab-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2fab-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2fab-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f2fab-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2fab-117">-VMName</span></span>
<span data-ttu-id="f2fab-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="f2fab-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="f2fab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fab-119">CommonParameters</span></span>
<span data-ttu-id="f2fab-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2fab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2fab-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2fab-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fab-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2fab-122">INPUTS</span></span>

### <span data-ttu-id="f2fab-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f2fab-123">System.String</span></span>

## <span data-ttu-id="f2fab-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2fab-124">OUTPUTS</span></span>

### <span data-ttu-id="f2fab-125">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2fab-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f2fab-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2fab-126">NOTES</span></span>

## <span data-ttu-id="f2fab-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2fab-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2fab-128">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f2fab-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="f2fab-129">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f2fab-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


