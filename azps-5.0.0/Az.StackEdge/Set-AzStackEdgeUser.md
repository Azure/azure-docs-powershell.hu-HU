---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187197"
---
# <span data-ttu-id="3d66b-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3d66b-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="3d66b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d66b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d66b-103">Új jelszó beállítása egy felhasználóhoz az eszközön.</span><span class="sxs-lookup"><span data-stu-id="3d66b-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="3d66b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d66b-104">SYNTAX</span></span>

### <span data-ttu-id="3d66b-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d66b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d66b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d66b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d66b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d66b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d66b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d66b-108">DESCRIPTION</span></span>
<span data-ttu-id="3d66b-109">A **set-AzStackEdgeUser** parancsmag új jelszót állít be a felhasználó számára a halom szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="3d66b-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="3d66b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3d66b-110">EXAMPLES</span></span>

### <span data-ttu-id="3d66b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3d66b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="3d66b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d66b-112">PARAMETERS</span></span>

### <span data-ttu-id="3d66b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d66b-113">-AsJob</span></span>
<span data-ttu-id="3d66b-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3d66b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d66b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d66b-115">-DefaultProfile</span></span>
<span data-ttu-id="3d66b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d66b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d66b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3d66b-117">-DeviceName</span></span>
<span data-ttu-id="3d66b-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="3d66b-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d66b-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3d66b-119">-EncryptionKey</span></span>
<span data-ttu-id="3d66b-120">Az Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="3d66b-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="3d66b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d66b-121">-InputObject</span></span>
<span data-ttu-id="3d66b-122">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="3d66b-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d66b-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d66b-123">-Name</span></span>
<span data-ttu-id="3d66b-124">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="3d66b-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d66b-125">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="3d66b-125">-Password</span></span>
<span data-ttu-id="3d66b-126">Jelszó – biztonságos karakterlánc biztosítása</span><span class="sxs-lookup"><span data-stu-id="3d66b-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="3d66b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d66b-127">-ResourceGroupName</span></span>
<span data-ttu-id="3d66b-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3d66b-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d66b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d66b-129">-ResourceId</span></span>
<span data-ttu-id="3d66b-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d66b-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d66b-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d66b-131">-Confirm</span></span>
<span data-ttu-id="3d66b-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d66b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d66b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d66b-133">-WhatIf</span></span>
<span data-ttu-id="3d66b-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d66b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d66b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d66b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d66b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d66b-136">CommonParameters</span></span>
<span data-ttu-id="3d66b-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d66b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d66b-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d66b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d66b-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d66b-139">INPUTS</span></span>

### <span data-ttu-id="3d66b-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d66b-140">None</span></span>

## <span data-ttu-id="3d66b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d66b-141">OUTPUTS</span></span>

### <span data-ttu-id="3d66b-142">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3d66b-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="3d66b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d66b-143">NOTES</span></span>

## <span data-ttu-id="3d66b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d66b-144">RELATED LINKS</span></span>
