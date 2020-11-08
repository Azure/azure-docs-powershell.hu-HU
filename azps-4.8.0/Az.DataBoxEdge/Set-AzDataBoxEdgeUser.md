---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185052"
---
# <span data-ttu-id="8cfa3-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8cfa3-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="8cfa3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cfa3-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfa3-103">Új jelszó beállítása egy felhasználóhoz az eszközön.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="8cfa3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cfa3-104">SYNTAX</span></span>

### <span data-ttu-id="8cfa3-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8cfa3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cfa3-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cfa3-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cfa3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cfa3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cfa3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cfa3-108">DESCRIPTION</span></span>
<span data-ttu-id="8cfa3-109">A **set-AzDataBoxEdgeUser** parancsmag új jelszót állít be a felhasználó számára az adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="8cfa3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8cfa3-110">EXAMPLES</span></span>

### <span data-ttu-id="8cfa3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8cfa3-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="8cfa3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cfa3-112">PARAMETERS</span></span>

### <span data-ttu-id="8cfa3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cfa3-113">-AsJob</span></span>
<span data-ttu-id="8cfa3-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8cfa3-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfa3-115">-DefaultProfile</span></span>
<span data-ttu-id="8cfa3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cfa3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8cfa3-117">-DeviceName</span></span>
<span data-ttu-id="8cfa3-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="8cfa3-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8cfa3-119">-EncryptionKey</span></span>
<span data-ttu-id="8cfa3-120">Az Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="8cfa3-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cfa3-121">-InputObject</span></span>
<span data-ttu-id="8cfa3-122">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="8cfa3-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8cfa3-123">-Name</span></span>
<span data-ttu-id="8cfa3-124">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="8cfa3-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-125">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="8cfa3-125">-Password</span></span>
<span data-ttu-id="8cfa3-126">Jelszó – biztonságos karakterlánc biztosítása</span><span class="sxs-lookup"><span data-stu-id="8cfa3-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cfa3-127">-ResourceGroupName</span></span>
<span data-ttu-id="8cfa3-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8cfa3-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cfa3-129">-ResourceId</span></span>
<span data-ttu-id="8cfa3-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cfa3-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfa3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8cfa3-131">-Confirm</span></span>
<span data-ttu-id="8cfa3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cfa3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cfa3-133">-WhatIf</span></span>
<span data-ttu-id="8cfa3-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cfa3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cfa3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfa3-136">CommonParameters</span></span>
<span data-ttu-id="8cfa3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cfa3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfa3-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfa3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cfa3-139">INPUTS</span></span>

### <span data-ttu-id="8cfa3-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="8cfa3-140">None</span></span>

## <span data-ttu-id="8cfa3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cfa3-141">OUTPUTS</span></span>

### <span data-ttu-id="8cfa3-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8cfa3-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="8cfa3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cfa3-143">NOTES</span></span>

## <span data-ttu-id="8cfa3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cfa3-144">RELATED LINKS</span></span>
